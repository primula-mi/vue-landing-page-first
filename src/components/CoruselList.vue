<template>
  <div class="vue-slide" ref="contentRef">
    <ul
      class="content"
      :style="{
        transform: `translate3d(${slideX}px, 0px, 0px)`,
        transition: `transform ${transition / 1000}s ${type}`,
      }"
      @touchstart="touchStart"
      @touchmove="touchMove"
      @touchend="touchEnd"
      @transitionend="transitionEnd"
    >
      <li><img :src="prevItem" /></li>
      <li><img :src="data[cur]" @click="$emit('click', cur)" /></li>
      <li><img :src="nextItem" /></li>
    </ul>
    <ul v-if="spot" class="spot">
      <li
        v-for="(d, i) in data.length"
        :class="{
          cur: i === cur,
        }"
        :key="i"
      ></li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    data: {
      // eslint-disable-next-line vue/require-valid-default-prop
      default: [],
      type: Array,
    },
    time: {
      default: 10000,
      type: Number,
    },
    speed: {
      default: 300,
      type: Number,
    },
    spot: {
      default: true,
      type: Boolean,
    },
    type: {
      default: "ease",
      type: String,
    },
    clockwise: {
      default: true,
      type: Boolean,
    },
  },
  data() {
    return {
      cur: 0,
      slideX: 0,
      transition: 0,
      touch: {
        startX: 0, // 触摸的初始位置 X
        startY: 0, // 触摸的初始位置 Y
        ifN: false, // 确定是否需要触摸移动的时候需要判断
        direction: false, // 确定是向上滚动还是向下滚动
        timer: null, // 定时滚动的定时器
        duration: 0, // 触摸了时间
        scrollDirection: false, // 滚动方向
      },
    };
  },
  mounted() {
    this.setTimer();
  },
  computed: {
    prevItem() {
      const item = this.data[this.cur - 1];
      return item ? item : this.data[this.data.length - 1];
    },
    nextItem() {
      const item = this.data[this.cur + 1];
      return item ? item : this.data[0];
    },
  },
  methods: {
    getGap(x, y = 0) {
      return parseInt((x - y).toString().replace("-", ""));
    },
    touchStart(e) {
      this.touch.startX = e.touches[0].clientX;
      this.touch.startY = e.touches[0].clientY;
      this.touch.ifN = true;
      this.touch.duration = new Date().getTime();
      window.clearInterval(this.touch.timer);
      this.transition = 0;
    },
    touchMove(e) {
      if (this.touch.ifN) {
        if (
          this.getGap(e.touches[0].clientX, this.touch.startX) >=
          this.getGap(e.touches[0].clientY, this.touch.startY)
        ) {
          this.touch.direction = true;
          e.currentTarget.style.transition = "";
        } else this.touch.direction = false;
        this.touch.ifN = false;
      } else {
        if (this.touch.direction) {
          e.preventDefault();
          this.slideX = e.touches[0].clientX - this.touch.startX;
        }
      }
    },
    touchEnd() {
      this.setTimer();
      if (!this.touch.direction) return;
      const time = new Date().getTime() - this.touch.duration;
      if (
        time > 300 &&
        this.getGap(this.slideX) < this.$refs.contentRef?.offsetWidth / 3
      ) {
        this.touch.scrollDirection = false;
        this.transition = this.speed * 0.8;
        this.slideX = 0;
      } else {
        if (this.slideX !== 0) {
          this.slideX > 0 ? this.prev() : this.next();
        }
      }
    },
    prev() {
      this.touch.scrollDirection = "prev";
      this.transition = this.speed;
      this.slideX = this.$refs.contentRef?.offsetWidth;
    },
    next() {
      this.touch.scrollDirection = "next";
      this.transition = this.speed;
      this.slideX = -this.$refs.contentRef?.offsetWidth;
    },
    transitionEnd() {
      let cur = 0;
      if (this.touch.scrollDirection === false) {
        cur = this.cur;
      } else {
        if (this.touch.scrollDirection === "prev") {
          if (this.cur === 0) {
            cur = this.data.length - 1;
          } else {
            cur = this.cur - 1;
          }
          this.$emit("prev", cur);
        } else {
          if (this.cur !== this.data.length - 1) {
            cur = this.cur + 1;
          }
          this.$emit("next", cur);
        }
      }
      if (this.cur !== cur) {
        this.$emit("change", cur);
      }
      this.transition = 0;
      this.slideX = 0;
      this.cur = cur;
    },
    setTimer() {
      if (this.time) {
        this.touch.timer = setInterval(
          this.clockwise ? this.next : this.prev,
          this.time
        );
      }
    },
  },
};
</script>
<style scoped>
.vue-slide {
  overflow: hidden;
  position: relative;
}
.vue-slide .content {
  display: flex;
  width: 300%;
}
.vue-slide .content > li {
  width: 33.33333%;
  position: relative;
}
.vue-slide .content > li:first-child {
  margin-left: -33.33333%;
}
.vue-slide .content img {
  display: block;
  width: 100%;
}
.vue-slide .spot {
  width: 100%;
  position: absolute;
  bottom: 12px;
  display: flex;
  justify-content: center;
}
.vue-slide .spot > li {
  width: 5px;
  height: 5px;
  border: 1px solid #fff;
  border-radius: 50%;
  margin: 0 4px;
  box-shadow: 0 0 3px rgba(0, 0, 0, 0.2);
  transition: width 0.2s linear;
}
.vue-slide .spot > li.cur {
  width: 12px;
  border-radius: 6px;
  background-color: #fff;
}
</style>

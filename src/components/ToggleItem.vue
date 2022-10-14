<template>
  <div class="toggle-menu__item" id="toggle">
    <span></span>
  </div>
</template>

<style scoped>
#toggle {
  display: flex;
  align-items: center;
  width: 28px;
  height: 30px;
}
#toggle span:after,
#toggle span:before {
  content: "";
  position: absolute;
  left: 0;
  top: -9px;
}
#toggle span:after {
  top: 9px;
}
#toggle span {
  position: relative;
  display: block;
}
#toggle span,
#toggle span:after,
#toggle span:before {
  width: 100%;
  height: 3px;
  background-color: #fff;
  transition: all 0.3s;
  backface-visibility: hidden;
  border-radius: 2px;
}
#toggle.active span {
  background-color: transparent;
}
#toggle.active span:before {
  transform: rotate(45deg) translate(5px, 5px);
}
#toggle.active span:after {
  transform: rotate(-45deg) translate(7px, -8px);
}
</style>

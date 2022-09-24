<template>
  <nav class="nav-menu">
    <ul class="nav-menu__list">
      <li class="nav-menu__item">
        <a class="nav-menu__link" href="#features">Features</a>
      </li>
      <li class="nav-menu__item">
        <a class="nav-menu__link" href="#about">About</a>
      </li>
      <li class="nav-menu__item">
        <a class="nav-menu__link" href="#pricing">Pricing</a>
      </li>
      <li class="nav-menu__item">
        <a class="nav-menu__link" href="#reviews">Reviews</a>
      </li>
      <li class="nav-menu__item">
        <a class="nav-menu__link" href="#contact">Contact</a>
      </li>
    </ul>
  </nav>
</template>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;600;700&display=swap");
.nav-menu {
  width: 40%;
}
.nav-menu__list {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 0;
  padding: 0;
}
.nav-menu__link {
  color: #b0b0b0;
  font-size: 1em;
  font-weight: 600;
  font-family: "Open Sans", "Arial", sans-serif;
}
</style>

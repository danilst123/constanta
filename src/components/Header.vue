<template>
  <header class="header">
    <h1 class="header__title">{{ title }}</h1>
    <Nav :isOpen="menuState" :clickHandle="toggleMenu" />
    <Hamburger :isActive="menuState" :clickHandle="toggleMenu" />
  </header>
</template>

<script>
import Nav from "./Nav";
import Hamburger from "./Hamburger";

export default {
  name: "header",
  props: {
    title: String
  },
  components: { Nav, Hamburger },
  data() {
    return {
      menuState: false
    };
  },
  methods: {
    toggleMenu: function() {
      console.log(this.menuState);
      this.menuState = !this.menuState;
    }
  }
};
</script>

<style lang="sass">
.header
  padding: 0 20px
  background-color: #333
  display: flex
  justify-content: space-between
  align-items: center
  height: 80px
  flex-shrink: 0
  @media screen and (max-width: 767px)
    height: 60px
  &__title
    margin: 0
    text-transform: uppercase
    color: #fff
    font-size: 26px
    line-height: 1.4
    @media screen and (max-width: 767px)
      font-size: 18px
</style>

<template>
  <nav id="nav" :class="{ nav: true, 'nav--opened': isOpen }">
    <div class="nav__item" @click="clickHandle">
      <router-link to="/">About</router-link>
    </div>
    <div class="nav__item" @click="clickHandle">
      <router-link to="/map">Map</router-link>
    </div>
  </nav>
</template>

<script>
export default {
  name: "nav",
  props: {
    isOpen: Boolean,
    clickHandle: Function
  }
};
</script>

<style lang="sass">
.nav
  @media screen and (max-width: 767px)
    display: none
  &__item
    display: inline-block
    margin: 10px
    a
      color: #fff
      text-decoration: none
      font-size: 24px
      text-transform: uppercase
      font-weight: 300
      &.router-link-exact-active
        text-decoration: underline
  &--opened
    @media screen and (max-width: 767px)
      display: flex
      flex-direction: column
      justify-content: center
      align-items: center
      padding: 20px
      position: fixed
      z-index: 10
      top: 0
      left: 0
      height: 100%
      width: 100%
      background: rgba(0, 0, 0, 0.5)
</style>

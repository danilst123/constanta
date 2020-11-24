<template>
  <div
    :class="{ hamburger: true, 'hamburger--active': isActive }"
    @click="clickHandle"
  >
    <div class="hamburger__item"></div>
    <div class="hamburger__item"></div>
    <div class="hamburger__item"></div>
  </div>
</template>

<script>
export default {
  name: "hamburger",
  props: {
    isActive: Boolean,
    clickHandle: Function
  }
};
</script>

<style lang="sass">
.hamburger
  height: 30px
  width: 30px
  position: relative
  cursor: pointer
  @media screen and (min-width: 768px)
    display: none
  &__item
    width: 100%
    height: 2px
    position: absolute
    z-index: 1
    top: 50%
    left: 0
    background: #fff
    transition: transform 0.3s
    &:nth-child(1)
      transform: translateY(calc(-50% - 10px))
    &:nth-child(2)
      transform: translateY(-50%)
    &:nth-child(3)
      transform: translateY(calc(-50% + 10px))
  &--active
    position: fixed
    z-index: 20
    top: 15px
    right: 20px
    .hamburger__item
      &:nth-child(1)
        transform: translateY(-50%) rotateZ(45deg)
      &:nth-child(2)
        transform: translateY(-50%) rotateZ(45deg)
      &:nth-child(3)
        transform: translateY(-50%) rotateZ(-45deg)
</style>

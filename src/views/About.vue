<template>
  <article class="about">
    <section class="about__section" :key="key" v-for="(info, key) in infos">
      <h2 class="about__subtitle">{{ info.sectionTitle }}</h2>
      <ul class="about__list">
        <li class="about__listItem" :key="key" v-for="(item, key) in info.data">
          {{ item }}
        </li>
      </ul>
    </section>
  </article>
</template>

<script>
export default {
  name: "about",
  data() {
    return {
      infos: [
        {
          sectionTitle: "skills",
          data: [
            "HTML",
            "CSS",
            "JavaScript",
            "Git",
            "jQuery",
            "React",
            "Sass",
            "Less",
            "Gulp",
            "Webpack",
            "Bootstrap",
            "Redux",
            "Адаптивная вёрстка",
            "BEM",
            "Avocode",
            "InVision",
            "Figma"
          ]
        },
        { sectionTitle: "Languages", data: ["Russian", "English"] }
      ]
    };
  }
};
</script>

<style lang="sass">
.about
  &__section
    margin-bottom: 30px
    &::last-child
      margin-bottom: 0
  &__subtitle
    text-transform: uppercase
    margin: 0 0 20px
  &__list
    list-style: none
    margin: 0 0 0 15px
    padding: 0
  &__listItem
    display: flex
    align-items: center
    margin-bottom: 5px
    &::last-child
      margin-bottom: 0
    &:before
      content: "—"
      margin-right: 10px
</style>

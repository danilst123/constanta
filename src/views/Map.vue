<template>
  <article class="map">
    <h2 class="map__title">
      Map
    </h2>
    <section class="map__map">
      <iframe
        src="https://yandex.ru/map-widget/v1/?um=constructor%3A7fad9028ec5fdc48d9c380eefc5152be8c80b928f0b1463fecc5f45cb93568ec&amp;source=constructor"
        width="100%"
        height="400"
        frameborder="0"
      ></iframe>
    </section>
  </article>
</template>

<script>
export default {
  data() {
    return {
      settings: {
        apiKey: "",
        lang: "ru_RU",
        coordorder: "latlong",
        version: "2.1"
      }
    };
  }
};
</script>

<style lang="sass">
.map
  &__title
    text-transform: uppercase
    margin: 0 0 20px
</style>

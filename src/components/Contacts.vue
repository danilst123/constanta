<template>
  <ul class="contacts">
    <li class="contacts__item" :key="key" v-for="(item, key) in contacts">
      {{ item }}
    </li>
    <li class="contacts__item">
      {{ new Date().toLocaleString() }}
    </li>
  </ul>
</template>

<script>
export default {
  name: "contacts",
  data() {
    return {
      contacts: ["+7 (906) 865-88-17", "dan_4324@mail.ru"]
    };
  }
};
</script>

<style lang="sass">
.contacts
  list-style: none
  margin: 0
  padding: 0
  font-size: 16px
  &__item + &__item
    margin-top: 10px
</style>

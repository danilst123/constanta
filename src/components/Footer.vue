<template>
  <footer class="footer">
    <Contacts />
  </footer>
</template>

<script>
import Contacts from "./Contacts";
export default {
  name: "footer",
  components: { Contacts }
};
</script>

<style lang="sass">
.footer
  padding: 20px
  background-color: #333
  color: #fff
  font-size: 20px
  line-height: 1.4
  flex-shrink: 0
</style>

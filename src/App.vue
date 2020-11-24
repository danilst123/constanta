<template>
  <div id="app" class="page">
    <Header title="Header" />
    <main class="main">
      <router-view />
    </main>
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header";
import Footer from "./components/Footer";

export default {
  name: "app",
  components: { Header, Footer }
};
</script>

<style lang="sass">
*
  box-sizing: border-box
body
  margin: 0
  font-family: Arial
  min-width: 320px
.page
  height: 100vh
  display: flex
  flex-direction: column
.main
  flex-grow: 1
  padding: 20px
</style>

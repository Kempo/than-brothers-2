<script setup>
import Title from "@/components/Title.vue";
import Menu from "@/components/Menu.vue";
import Locations from "@/components/Locations.vue";
import Contact from "@/components/Contact.vue";
import Footer from "@/components/Footer.vue"
</script>

<template>
  <main id="main">
    <Title />
    <Menu />
    <Locations />
    <Contact />
    <Footer />
  </main>
</template>

<style lang="scss">
@import "../assets/main.scss";

#main {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  height: 100%;
  width: 100%;
  font-family: $default-font;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-weight: $thin-default;
  overflow-x: hidden;
}
</style>

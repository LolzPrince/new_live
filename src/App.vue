<template>
  <div id="app">
    <header-menu></header-menu>
    <router-view/>
    <footer-menu></footer-menu>
  </div>
</template>
<script>
import HeaderMenu from "@/components/HeaderMenu";
import FooterMenu from "@/components/FooterMenu";
import("./assets/css/style.css")
export default {
  components:{
    HeaderMenu,
    FooterMenu
  },
}
</script>
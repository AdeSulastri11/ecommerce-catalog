<template>
  <div id="app">
    <NavbarMenu/>
    <HomePage />
    <AboutFashion/>
    <DisplayProduct/>
    <ContactUs/>
    <FooterWeb/>
  </div>
</template>

<script>
import HomePage from './components/Home.vue';
import NavbarMenu from './components/NavbarMenu.vue'
import AboutFashion from './components/About.vue';
import DisplayProduct from './components/DisplayProducts.vue';
import ContactUs from './components/Contact.vue';
import FooterWeb from './components/Footer.vue';
export default {
  name: 'App',
  components: {
    HomePage,
    NavbarMenu,
    AboutFashion,
    DisplayProduct,
    ContactUs,
    FooterWeb
  }
}
</script>

<style>
:root {
  --bg: #FFFFFF;
  --bg-unv: #DCDCDC;
  --bg-button-men: #002772;
  --bg-men: #D6E6FF;
  --bg-women: #FDE2FF;
  --bg-button-women: #720060;
  --headline: #1E1E1E;
  --paragraph: #3F3F3F;
}
body {
  margin: 0;
  padding: 0;
  background-color: var(--bg);
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  scroll-behavior: smooth;
}
</style>

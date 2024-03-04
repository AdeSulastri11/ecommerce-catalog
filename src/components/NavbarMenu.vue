<template>
  <header>
    <nav>
      <div class="logo">
        <img alt="logo ecommerce" src="../assets/logo.png">
      </div>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#product">Product</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
      <div class="search">
        <input type="search" name="search" id="search" placeholder="Search...">
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'NavbarMenu',
  props: {
  }
}
</script>

<style scoped>
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
@font-face {
  font-family: Demo;
  src: url('../assets/fonts/Demo_Fonts/Fontspring-DEMO-theseasons-bd.otf');
}
header {
  /* position: fixed; */
  top: 0;
  left: 0;
  right: 0;
  padding: 5px 70px;
}
nav {
  display: grid;
  align-items: center;
  justify-content: space-between;
  grid-template-columns: 1fr 2fr 1fr;
}
.logo, .search {
  display: flex;
  justify-content: flex-start;
}
.search {
  display: flex;
  justify-content: flex-end;
}
.search input{
  padding: 7px 10px;
  border-radius: 5px;
  border: 2px solid var(--bg-button-men);
}
nav img {
  max-width: 100%;
  width: 120px;
}
nav ul {
  display: flex;
  justify-content: center;
  column-gap: 20px;
}
nav ul li {
  list-style: none;
  display: inline-block;
}
nav ul li a {
  text-decoration: none;
  font-family: Demo;
  color: var(--headline);
}
</style>
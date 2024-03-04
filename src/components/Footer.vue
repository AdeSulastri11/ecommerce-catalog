<template>
  <footer>
    <div class="dots man"></div>
    <div>
      <img src="../assets/logo.png" alt="">
      <h3>Fashion Store</h3>
      <div class="socialMedia">
        <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"><path fill="currentColor" d="M19 3a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2zm-.5 15.5v-5.3a3.26 3.26 0 0 0-3.26-3.26c-.85 0-1.84.52-2.32 1.3v-1.11h-2.79v8.37h2.79v-4.93c0-.77.62-1.4 1.39-1.4a1.4 1.4 0 0 1 1.4 1.4v4.93zM6.88 8.56a1.68 1.68 0 0 0 1.68-1.68c0-.93-.75-1.69-1.68-1.69a1.69 1.69 0 0 0-1.69 1.69c0 .93.76 1.68 1.69 1.68m1.39 9.94v-8.37H5.5v8.37z"/></svg>
        <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"><path fill="currentColor" d="M20.9 2H3.1A1.1 1.1 0 0 0 2 3.1v17.8A1.1 1.1 0 0 0 3.1 22h9.58v-7.75h-2.6v-3h2.6V9a3.64 3.64 0 0 1 3.88-4a20.26 20.26 0 0 1 2.33.12v2.7H17.3c-1.26 0-1.5.6-1.5 1.47v1.93h3l-.39 3H15.8V22h5.1a1.1 1.1 0 0 0 1.1-1.1V3.1A1.1 1.1 0 0 0 20.9 2"/></svg>
        <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"><path fill="currentColor" d="M7.8 2h8.4C19.4 2 22 4.6 22 7.8v8.4a5.8 5.8 0 0 1-5.8 5.8H7.8C4.6 22 2 19.4 2 16.2V7.8A5.8 5.8 0 0 1 7.8 2m-.2 2A3.6 3.6 0 0 0 4 7.6v8.8C4 18.39 5.61 20 7.6 20h8.8a3.6 3.6 0 0 0 3.6-3.6V7.6C20 5.61 18.39 4 16.4 4zm9.65 1.5a1.25 1.25 0 0 1 1.25 1.25A1.25 1.25 0 0 1 17.25 8A1.25 1.25 0 0 1 16 6.75a1.25 1.25 0 0 1 1.25-1.25M12 7a5 5 0 0 1 5 5a5 5 0 0 1-5 5a5 5 0 0 1-5-5a5 5 0 0 1 5-5m0 2a3 3 0 0 0-3 3a3 3 0 0 0 3 3a3 3 0 0 0 3-3a3 3 0 0 0-3-3"/></svg>
      </div>
      <p>Ade Sulastri</p>
    </div>
    <div class="dots woman"></div>
  </footer>

</template>

<script>
export default {
  name: 'FooterWeb'
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
@font-face {
  font-family: Demo;
  src: url('../assets/fonts/Demo_Fonts/Fontspring-DEMO-theseasons-bd.otf');
}
footer {
  padding: 40px 70px;
  /* border: 1px solid; */
  overflow: hidden;
  margin-top: 70px;
  position: relative;
}

footer img {
  max-width: 100%;
  width: 120px;
}
footer h3 {
  font-family: Demo;
}
footer h3, .socialMedia p {
  margin: 0;
}
.dots {
  position: absolute;
  aspect-ratio: 1.1/1;
  width: 500px;
  border-radius: 100%;
  filter: blur(50px);
  z-index: -1;
}

.man {
  background-color: var(--bg-men);
  left: -30px;
  top: -10px;
}

.woman {
  background-color: var(--bg-women);
  top: -20px;
  right: 0;
  border: 1px solid;
}
</style>
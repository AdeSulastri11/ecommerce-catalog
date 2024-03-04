<template>
  <div class="contentHome">
    <div class="dot-blue"></div>
    <div class="dot-pink"></div>
    <div class="contentLeft">
      <Transition appear>
        <h1>Welcome to Fashion's Latest Trends</h1>
      </Transition>
      <p>Welcome to our latest fashion catalog! Discover your unique style with our newest collection. Enjoy your shopping
        experience with us!</p>
      <div class="btn">
        <button type="submit">Learn More</button>
      </div>
    </div>
    <div class="img-main">
      <img src="../assets/model-bg.png" alt="">
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomePage',
  props: {
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
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
  font-family: Libre Franklin;
  src: url('../assets/fonts/Libre_Franklin/LibreFranklin-VariableFont_wght.ttf');
}

@font-face {
  font-family: Demo;
  src: url('../assets/fonts/Demo_Fonts/Fontspring-DEMO-theseasons-bd.otf');
}

@font-face {
  font-family: Zoela;
  src: url('../assets/fonts/zoela/zoela.ttf.ttf');
}

.contentHome {
  display: grid;
  align-items: center;
  justify-content: space-between;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  height: 90vh;
  overflow: hidden;
  padding: 0 70px;
}

.dot-blue {
  position: absolute;
  width: 400px;
  aspect-ratio: 1/1;
  background-color: var(--bg-men);
  border-radius: 100%;
  filter: blur(100px);
  top: 0;
  right: 0;
  z-index: -1;
}
.dot-pink {
  position: absolute;
  width: 400px;
  aspect-ratio: 1/1;
  background-color: var(--bg-women);
  border-radius: 100%;
  filter: blur(100px);
  bottom: 0;
  left: 0;
  z-index: -1;
}

.contentHome img {
  width: 50rem;
}

.img-main {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: flex-end;
  margin-top: -100px;
}

.img-main img {
  max-width: 100%;
  width: 70%;
  
}

.contentLeft {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  row-gap: 15px;
  margin-top: -50px;
}
.contentLeft .btn button{
  padding: 10px 17px;
  border-radius: 5px;
  border: none;
  cursor: pointer;
  background-color: #5b88dbd7;
  color: var(--bg);
}
.contentLeft .btn button:active{
  background-color: #5c90f1;
  color: var(--bg);
}
.contentLeft h1,
p {
  margin: 0;
  text-align: left;
}

.contentLeft h1 {
  font-family: zoela;
  font-size: 300%;
  /* font-weight: 100; */
  line-height: 50px;
}
.contentLeft p {
  font-family: Libre Franklin;
  font-weight: 100;
}
.v-enter-active {
  animation: swirlAdded 2s;
}

@keyframes swirlAdded {
  from {
    opacity: 0;
    transform: translateY(-100px);
  }

  to {
    opacity: 1;
    transform: translateY(0);
  }
}</style>

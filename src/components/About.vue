<template>
  <div class="about">
    <div class="content">
      <div class="content-left">
        <h1>Fashion Store</h1>
        <p>Fashion Store adalah tempat yang sempurna untuk menemukan gaya terkini untuk pria dan wanita. Dari pakaian
          casual hingga gaun mewah, kami menawarkan berbagai koleksi yang memenuhi segala selera dan kebutuhan fashion
          Anda. Temukan produk berkualitas tinggi dengan desain terbaru dan harga yang terjangkau. Jelajahi toko kami
          sekarang dan temukan penampilan yang sesuai dengan gaya Anda!</p>
      </div>
      <div class="content-right">
        <div>
          <img src="../assets/img/img-woman.jpg" alt="">
        </div>
        <div>
          <img src="../assets/img/img-man.jpg" alt="">
        </div>
      </div>
    </div>

    <!-- <div class="man">
      <div class="content-left">
        <h2>Men's Clothing</h2>
        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Tempora excepturi minus quos eveniet ullam, sed
          possimus voluptatum enim nostrum. Sed?</p>
        <div class="btn">
          <button>See All</button>
        </div>
      </div>
      <div class="matrix">
        <div class="dot"></div>
        <div class="dot"></div>
        <div class="dot"></div>
        <div class="dot"></div>
        <div class="dot"></div>
        <div class="dot"></div>
        <div class="dot"></div>
        <div class="dot"></div>
        <div class="dot"></div>
      </div>
      <div class="img-man">
        <img src="../assets/img/model-man.png" alt="">
      </div>
    </div>
    <div class="woman">
      <div class="img-woman">
        <div class="matrix matrix-woman">
          <div class="dot"></div>
          <div class="dot"></div>
          <div class="dot"></div>
          <div class="dot"></div>
          <div class="dot"></div>
          <div class="dot"></div>
          <div class="dot"></div>
          <div class="dot"></div>
          <div class="dot"></div>
        </div>
        <img src="../assets/img/model-woman.png" alt="">
      </div>
      <div class="content-right">
        <h2>Women's Clothing</h2>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quisquam soluta et facere natus aperiam praesentium
          similique ratione mollitia eaque at.</p>
        <div class="btn">
          <button>See All</button>
        </div>
      </div>
    </div> -->
  </div>
</template>

<script>
export default {
  name: 'AboutFashion',
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
@font-face {
  font-family: Libre Franklin;
  src: url('../assets/fonts/Libre_Franklin/LibreFranklin-VariableFont_wght.ttf');
}
.about {
  padding: 80px 70px;
}
.content {
  display: grid;
  align-items: center;
  justify-content: space-between;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
}
.content-left h1, p {
  margin: 5px;
}
.content-left h1 {
  font-family: Demo;
  text-align: left;
}
.content-left p {
  font-family: Libre Franklin;
  font-size: 15px;
  text-align: justify;
  font-weight: 100;
}
.content-right {
  position: relative;
  overflow: hidden;
  display: flex;
  justify-content: flex-end;
  column-gap: 20px;
}
.content-right img {
  width: 200px;
}
/* .man,
.woman {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
}

.img-man .img-woman {
  border: 1px solid;
}

.matrix {
  display: grid;
  grid-template-columns: repeat(3, 20px);
  grid-template-rows: repeat(3, 20px);
  gap: 8px 5px;
  position: absolute;
}

.dot {
  aspect-ratio: 1/1;
  width: 6px;
  border-radius: 100%;
  background-color: var(--bg-button-men);
}

.matrix-woman .dot {
  background-color: var(--bg-button-women);
}

.content-left,
.content-right {
  display: flex;
  justify-content: center;
  flex-direction: column;
}

.man img,
.woman img {
  max-width: 50%;
  width: 200px;
}

.img-woman::before {
  content: "";
  position: absolute;
  border: 3px solid var(--bg-button-women);
  height: 50%;
  width: 22%;
  z-index: 1;
  overflow: hidden;
} */
</style>
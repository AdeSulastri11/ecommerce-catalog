<template>
  <div class="container-product " id="product">
    <!-- <div > -->
    <TransitionGroup mode="out-in" class="card-product">
      <div v-for="product in products" :key="product.id">
        <div
          :class="{ 'men-section': product.category === 'men\'s clothing', 'women-section': product.category === 'women\'s clothing' }">
          <div v-if="product.category === 'men\'s clothing' || product.category === 'women\'s clothing'"
            v-show="currentIndex === product.id" class="card-product-layer2">
            <div class="product">
              <div class="img-product">
                <img :src=product.image alt="">
              </div>
              <div class="content-product">
                <h3>{{ product.title }}</h3>
                <div class="detail">
                  <p>{{ product.category }}</p>
                  <div class="rating">
                    <p>{{ product.rating.rate }}</p>
                  </div>
                </div>
                <hr>
                <p class="description">{{ product.description }}</p>
                <hr>
                <p class="price">${{ product.price }}</p>
                <div class="btn">
                  <button>Buy now</button>
                  <button @click="nextProduct">Next product</button>
                </div>
              </div>
            </div>
          </div>
          <div v-if="product.category === 'jewelery' || product.category === 'electronics'"
            :class="{ 'unavailable-section-jewelery': product.category === 'jewelery', 'unavailable-section-electronics': product.category === 'electronics' }">
            <div v-if="currentIndex === product.id">
              <div class="container-card">
                <div class="card-unavailable">
                  <div class="content-unavailable">
                    <p>This product is unavailable to show</p>
                    <div class="btn">
                      <button @click="nextProduct">Next product</button>
                    </div>
                  </div>
                </div>
              </div>
            </div>

          </div>
        </div>
      </div>
    </TransitionGroup>
    <!-- </div> -->
  </div>

</template>

<script>
import axios from 'axios'
import { TransitionGroup } from 'vue';

export default {
  name: 'DisplayProduct',
  comments: {
    TransitionGroup
  },
  data() {
    return {
      products: [],
      currentIndex: 1
    }
  },
  created() {
    axios.get('https://fakestoreapi.com/products')
      .then(response => {
        // this.products = response.data;
        // console.log(this.products)
        response.data.forEach(product => {
          if (product.category === "men's clothing") {
            this.products.push(product)
          } else if (product.category === "women's clothing") {
            this.products.push(product)
          } else if (product.category === "electronics" || product.category === "jewelery") {
            this.products.push(product)
          }
        });
      })
      .catch(error => {
        console.error('Error fetching data', error);
      })
  },
  methods: {
    nextProduct() {
      this.currentIndex++
      if (this.currentIndex >= this.products.length) {
        this.currentIndex = 1
      }
    }
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

.container-product {
  position: relative;
  height: 80vh;
  overflow: hidden;
  display: flex;
  justify-content: center;
  padding-top: 50px;
}

.product {
  box-shadow: 0 1px 5px 5px var(--bg-unv);
  display: flex;
  padding: 20px;
  width: 600px;
  height: 350px;
  border-radius: 5px;
  justify-content: center;
  background-color: var(--bg);
}

.card-product img {
  width: 180px;
}

.img-product {
  padding: 0 5px;
  display: flex;
  align-items: center;
  flex: 20px;
}

.content-product {
  text-align: start;
  padding: 0 20px;
  flex: 150px;
}

.content-product .description {
  height: 125px;
  font-size: 15px;
}

.detail {
  display: flex;
  justify-content: space-between;
}

.detail p {
  margin: 0;
}

.price {
  margin: 5px;
  font-weight: bold;
}

.btn {
  gap: 20px;
  display: flex;
}

.card-product {
  height: 45vh;
  width: 100%;
}

.card-product-layer2 {
  width: 100vw;
  height: 50vh;
  display: flex;
  justify-content: center;
  padding-top: 50px;
}

.content-product h3 {
  height: 45px;
}

/* men section */
.men-section .btn button {
  padding: 7px;
  width: 100%;
  border: none;
  border-radius: 5px;
  background-color: var(--bg-button-men);
  color: var(--bg);
  cursor: pointer;
}

.men-section .btn button:nth-child(2) {
  background-color: white;
  border: 2px solid var(--bg-button-men);
  color: var(--headline);
}

.men-section .content-product h3 {
  color: var(--bg-button-men);
}

.men-section .card-product {
  height: 45vh;
  background-color: var(--bg-men);
}

.men-section .card-product-layer2 {
  background-color: var(--bg-men);
}

.men-section .card-product {
  background-color: var(--bg-men);
}

/* women section */
.women-section .btn button {
  padding: 7px;
  width: 100%;
  border: none;
  border-radius: 5px;
  background-color: var(--bg-button-women);
  color: var(--bg);
  cursor: pointer;
}

.women-section .btn button:nth-child(2) {
  background-color: white;
  border: 2px solid var(--bg-button-women);
  color: var(--headline);
}

.women-section .content-product h3 {
  color: var(--bg-button-women);
}

.women-section .description {
  overflow-y: scroll;
}

.women-section .description::-webkit-scrollbar {
  background-color: var(--bg);
}

.women-section .card-product-layer2 {
  background-color: var(--bg-women);
}

/* unvailable */
.container-card {
  padding-top: 50px;
  background-color: var(--bg-unv);
  height:50vh;
  width: 100%;
}
.card-unavailable {
  position: relative;
  box-shadow: 0 1px 5px 5px var(--bg-unv);
  display: flex;
  padding: 20px;
  border-radius: 5px;
  background-image: url('../assets/img/sad-face.png');
  background-size: 75%;
  background-repeat: no-repeat;
  background-position: center;
  width: 600px;
  height: 350px;
  justify-content: center;
  background-color: var(--bg);
}

.unavailable-section-jewelery .img-sad-face,
.unavailable-section-electronics .img-sad-face {
  width: 100%;
  background-position: center;
  margin: auto;
}

.unavailable-section-jewelery,
.unavailable-section-electronics {
  display: flex;
  justify-content: center;
  background-color: var(--bg-unv);
}

.unavailable-section-jewelery .content-unavailable,
.unavailable-section-electronics .content-unavailable {
  padding: 7px;
  width: 100%;
  border: none;
  border-radius: 5px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.content-unavailable .btn button {
  cursor: pointer;
  padding: 3px 100px;
  border-radius: 3px;
  background-color: var(--bg);
  border: 2px solid var(--headline);
  color: var(--headline);
}
.content-unavailable .btn button:active {
  background-color: var(--bg-unv);
}

.card-unavailable .content-unavailable p {
  margin: 5px;
}

.v-enter-active {
  animation: swirlAdded 0.7s;
}

.v-leave-active {
  animation: swirlAdded 0.7s reverse;
}

@keyframes swirlAdded {
  from {
    opacity: 0;
    transform: translateX(200px);
  }

  to {
    opacity: 1;
    transform: translateX(0);
  }
}
</style>
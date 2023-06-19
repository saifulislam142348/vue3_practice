<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Welcome to Your Vue.js App" />
  <ContactView name="kamal" />
  <TheCard name="saiful islam">
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Eaque odio
      voluptatum animi natus soluta alias laudantium pariatur sit est
      accusantium ipsam, eum nostrum? Distinctio blanditiis sint ab impedit quas
      fugit quam dolor culpa labore excepturi dolorum reprehenderit voluptate
      placeat expedita asperiores sunt in laborum facere, sit veritatis suscipit
      qui tempore?
    </p>
  </TheCard>
  <TheCard name="title nme">
    <template v-slot:info>
      <p>
        laudantium pariatur sit est accusantium ipsam, eum nostrum? Distinctio
        blanditiis sint ab impedit quas fugit quam dolor culpa labore excepturi
        dolorum reprehenderit voluptate placeat expedita asperiores sunt in
        laborum facere, sit veritatis suscipit qui tempore?
      </p>
    </template>
  </TheCard>
  <Product-Card
    v-for="product in products"
    :key="product.name"
    :product="product"
    @buy_click="buyNow"
    @cart_click="cartadd"
    @fvt="addFvtChange"
  >
  </Product-Card>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import ContactView from "./components/ContactView.vue";
import TheCard from "./components/TheCard.vue";
import ProductCard from "./components/ProductCard.vue";

export default {
  data() {
    return {
      products: [
        {
          name: "Iphone pro 14 max",
          tumbail: "img/sm.jpg",
          price: "2777",
          addFvt: true,
        },
        {
          name: "Samsung x",
          tumbail: "img/ip.jpg",
          price: "40077",
          addFvt: false,
        },
      ],
    };
  },
  name: "App",
  components: {
    HelloWorld,
    ContactView,
    TheCard,
    ProductCard,
  },
  methods: {
    buyNow(product) {
      console.log(product);
    },
    cartadd(product) {
      console.log(product);
    },
    addFvtChange(product) {
      product.addFvt = !product.addFvt;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

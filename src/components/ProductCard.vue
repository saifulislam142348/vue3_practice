<template>
  <div class="product-card">
    <div class="product-card_title d-flex flex-row">
      <div class="p-2">{{ product.name }}</div>
      <div class="p-2">
        <img
          src="img/star.png"
          alt=""
          v-if="product.addFvt"
          @click="$emit('fvt', product)"
          style="height: 30px; width: 30px"
        />
        <img
          src="img/un_star.png"
          v-else
          @click="$emit('fvt', product)"
          alt=""
          style="height: 30px; width: 30px"
        />
      </div>
    </div>
    <div class="product-card_body">
      <img :src="product.tumbail" style="width: 50%" alt="" />
      <p class="padding:4px">price: {{ product.price }}</p>
    </div>
    <div class="product-card_footer">
      <button
        class="btn btn-dark btn-outline-success"
        @click="$emit('buy_click', product)"
      >
        Buy now
      </button>
      <button
        class="btn btn-dark btn-outline-danger"
        @click="$emit('cart_click', product)"
      >
        Cart Add
      </button>
    </div>
  </div>
</template>
<script>
export default {
  name: "Product-Card",
  data() {
    return {};
  },
  props: { product: { type: Object, default: () => {} } },
  methods: {
    add() {
      console.log("changing");
    },
  },
};
</script>
<style scope>
.product-card {
  width: 300px;
  min-height: 100px;
  margin: 22px auto;
  border: 1px solid black;
}
.product-card_title {
  background: green;
  padding: 5px 11px;
  color: azure;
}
.product-card_body {
  padding: 11px;
}
.product-card_body img {
  height: 111px;
}
.product-card_footer {
  padding: 5px 11px;
}
</style>

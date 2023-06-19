<template>
  <div class="product-card">
    <div class="product-card_title">{{ product.name }}</div>
    <div class="product-card_body">
      <img :src="product.tumbail" style="width: 50%" alt="" />
      <p class="padding:4px">price: {{ product.price }}</p>
    </div>
    <div class="product-card_footer">
      <button class="btn btn-dark btn-outline-success">Buy now</button>
      <button class="btn btn-dark btn-outline-danger">Cart Add</button>
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
};
</script>
<style scope>
.product-card {
  width: 300px;
  min-height: 100px;
  margin: 22px auto;
}
.product-card_title {
  background: green;
  padding: 5px 11px;
  color: azure;
}
.product-card_body {
  padding: 11px;
  background: rgb(156, 151, 151);
}
.product-card_body img {
  height: 111px;
}
.product-card_footer {
  background: yellow;
  padding: 5px 11px;
}
</style>

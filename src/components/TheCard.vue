<template>
  <h2>Card</h2>
  <div class="content">
    <div class="card">
      <div class="header">
        <p>name:{{ name }}</p>
      </div>
      <slot></slot>
      <div class="footer">
        <slot name="info"></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["name"],
};
</script>

<style scoped>
.content {
  margin: 10px;
  background-color: blue;
  padding: 30px;
  width: 100%;
  height: 300px;
  border: 2px solid rgb(37, 214, 51);
  position: relative;
}

.card {
  margin: 10px;
  background-color: rgb(188, 188, 192);
  width: 300px;
  height: 300px;
  border: 2px solid red;
  float: left;
}
h1 {
  background-color: black;
}
.header {
  background-color: blueviolet;
  width: auto;
  max-height: 50px;
  padding: 2px;
}
</style>

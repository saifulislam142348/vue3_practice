<template>
<h2>Card</h2>


<div class="content">
<div class="card">
<slot name="default"></slot>
  <p>name:{{ name }}</p>
<slot name="info"></slot>
</div>
  
</div>
</template>

<script>
export default {
  props: ['name']
}
</script>

<style >
.content{
  margin: 10px;
  background-color: blue;
  padding: 30px;
  width: 100%;
  height: 300px;
  border: 2px solid rgb(37, 214, 51);
position: relative;
}
.card{
   margin: 10px;
  background-color: rgb(188, 188, 192);
  width: 300px;
  height: 300px;
  border: 2px solid red;
  float: left;

}
h1{
  background-color: black;
}
</style>
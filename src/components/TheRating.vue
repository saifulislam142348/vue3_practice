<template>
  <div class="rating">
    <div
      class="rating-star"
      v-for="index in 5"
      :key="index"
      @click="$emit('update:modelValue', index)"
    >
      <img src="img/star.png" alt="" v-if="index <= modelValue" />
      <img src="img/un_star.png" alt="" v-if="index > modelValue" />
    </div>
  </div>
</template>

<script>
export default {
  name: "The-Rating",
  props: {
    modelValue: {
      type: Number,
      default: 0,
    },
  },
  emits: ["update:modelValue"],
};
</script>

<style>
.rating {
  width: 200px;
  display: flex;
  align-items: center;
}
.rating-star {
  cursor: pointer;
  margin: 2px;
}
.rating-star img:hover {
  transform: (1, 1);
}
</style>

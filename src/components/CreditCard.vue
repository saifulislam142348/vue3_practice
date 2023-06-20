<template>
  <div class="CreditCard">
    <input
      class="form-control"
      type="text"
      :value="nameOnCard"
      placeholder="NAme On Card"
      @input="$emit('update:nameOnCard', $event.target.value)"
    />
    <input
      class="form-control"
      type="number"
      :value="cardNumber"
      placeholder="card number"
      @input="$emit('update:cardNumber', $event.target.value)"
    />
    <input
      class="form-control"
      type="date"
      :value="expiry"
      placeholder="expiry"
      @input="$emit('update:expiry', $event.target.value)"
    />
    <input
      class="form-control"
      type="text"
      :value="cvv"
      placeholder="cvv"
      @input="$emit('update:cvv', $event.target.value)"
    />
  </div>
</template>

<script>
export default {
  name: "CreditCard",
  props: {
    nameOnCard: { type: String, default: "" },
    cardNumber: { type: String, default: () => {} },
    expiry: { type: Date, default: "" },
    cvv: { type: String, default: "" },
  },
};
</script>

<style></style>

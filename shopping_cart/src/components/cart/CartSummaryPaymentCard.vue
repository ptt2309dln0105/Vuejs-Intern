<template>
  <div class="cart-iem-card">
    <h3>Cart Total : $ {{ cart_total.toFixed(2) }}</h3>
    <button class="view-product-button">Pay by Credit Card</button>
  </div>
</template>

<script>
export default {
  props: ["products"],
  computed: {
    cart_total() {
      return this.$store.getters.cartTotal;
    },
  },
};
</script>

<style></style>

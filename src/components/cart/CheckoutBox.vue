<template>
  <div>
    <v-card outlined>
      <v-card-title>Payment Details</v-card-title>

      <v-card-text>
        <p>Total: ${{ total }}</p>
        <v-text-field label="name" />
        <v-text-field label="email" />
        <v-btn color="primary" @click="goToCheckout">Checkout</v-btn>
      </v-card-text>
    </v-card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      checkoutForm: null,
      nameRules: [],
      name: "",
      emailRules: [],
      email: "",
      total: 999,
    };
  },
  methods: {
    goToCheckout() {
      this.$router.push({ name: "checkout" });
    },
  },
};
</script>

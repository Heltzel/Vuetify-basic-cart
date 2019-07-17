<template>
  <v-container>

    <v-toolbar color="light-green  " dark  class=" mb-4  darken-2 ">
      <v-toolbar-title><h2 class="font-weight-light">Basket checkout</h2></v-toolbar-title>
      <v-spacer></v-spacer>
    </v-toolbar>

    <form action="">
      <v-layout >
        <v-flex x6 class="mx-4">
          <strong>Payment Adress: </strong>
          <v-text-field label="Name"></v-text-field>
          <v-text-field label="Address"></v-text-field>
          <v-text-field label="Zipcode"></v-text-field>
          <v-text-field label="City"></v-text-field>
          <v-text-field label="Phone"></v-text-field>
          <v-text-field label="Email"></v-text-field>
          <v-checkbox v-model="delivery_address" label="Other Delivery Address"></v-checkbox>
        </v-flex>
        <v-flex x6 class="mx-4">
          <strong>Delivery Adress:</strong>
          <div v-if="delivery_address">
            <v-text-field label="Name"></v-text-field>
            <v-text-field label="Address"></v-text-field>
            <v-text-field label="Zipcode"></v-text-field>
            <v-text-field label="City"></v-text-field>
          </div>
          <div v-else>
            <v-alert type="info" :value="true">
              The delivery address is the same as the payment address.
            </v-alert>
          </div>
          <v-container>
            <v-btn color="success" large ripple style="float:right;"> Complete Order </v-btn>
          </v-container>
        </v-flex>
      </v-layout>
     
    </form>
  
  </v-container>
</template>

<script>
  export default {
    name: "BasketCheckout",
    data() {
      return {
        delivery_address: false
      }
    },
  }
</script>

<style scoped>
  
</style>

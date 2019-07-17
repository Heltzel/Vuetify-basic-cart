<template>
  <v-container>
    <v-toolbar color="blue lighten-3" dark  class=" mb-4  darken-2 ">
      <v-toolbar-title><h2 class="font-weight-light">My Basket</h2></v-toolbar-title>
      <v-spacer></v-spacer>
    </v-toolbar>

    <v-list two-line>
      <template v-for="(product, index) in products">
        <v-list-tile :key="product.product_id" avatar>

          <v-list-tile-avatar :tile = true >
            <img :src="product.img" >
          </v-list-tile-avatar>

          <v-list-tile-content>
            <v-list-tile-title v-html="product.title"></v-list-tile-title>
            <v-list-tile-sub-title v-html="product.sub_title"></v-list-tile-sub-title>
          </v-list-tile-content>

          <v-list-tile>
            &euro; {{ product.price}}
          </v-list-tile>

          <v-list-tile-action>
            <V-text-field label="Quantity" reverse :value="product.qty">
            </V-text-field>
          </v-list-tile-action>

          <v-list-tile>
            &euro; {{ product.price * product.qty}}
          </v-list-tile>

         <v-list-tile-action>
            <v-btn color="red lighten-1" class="white--text" icon ripple>
                  <v-icon>mdi-delete</v-icon>
                </v-btn>
         </v-list-tile-action>

        </v-list-tile>
        <v-divider v-if="index + 1 < products.length" :key="index"></v-divider>
      </template>
    </v-list>
   
   <v-container>
     <v-btn color="success" to="/basket/checkout" style="float:right;"> Go To Payment</v-btn>
   </v-container>

  </v-container>
</template>

<script>
  export default {
    data() {
      return {
        products:[
          {
            product_id: "kitchen_1",
            img: "https://cdn.vuetifyjs.com/images/cards/kitchen.png",
            title: "QW cooking utensils",
            sub_title: "Our Vintage kitchen utensils delight any chef.\n Made of bamboo by hand",
            price: 14.99,
            qty: 1
          },
          {
            product_id: "kitchen_4",
            img: "https://cdn.vuetifyjs.com/images/cards/kitchen.png",
            title: "QW cooking utensils",
            sub_title: "Our Vintage kitchen utensils delight any chef.\n Made of bamboo by hand",
            price: 39.99,
            qty: 2
          },
          {
            product_id: "kitchen_6",
            img: "https://cdn.vuetifyjs.com/images/cards/kitchen.png",
            title: "QW cooking utensils",
            sub_title: "Our Vintage kitchen utensils delight any chef.\n Made of bamboo by hand",
            price: 17.99,
            qty: 1
          }
        ]
      }
    },
  }
</script>

<style scoped>
  a {
  color: white;
  text-decoration: none;
}
</style>

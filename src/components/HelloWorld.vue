
<template>
  <v-container>

    <v-toolbar color="orange" dark  class=" mb-4  darken-2 ">
      <v-toolbar-title><h2 class="font-weight-light">Hot products showing</h2></v-toolbar-title>
      <v-spacer></v-spacer>
    </v-toolbar>

    <v-layout row wrap>
      <template v-for="(product, index) in products" xs12>
        <v-flex xs12 md2 pa-1 :key="index">
          <v-hover>
            <v-card slot-scope="{ hover }" class="mx-auto" color="grey lighten-4" max-width="600">
              <v-img  :src="product.src" :aspect-ratio="16/9">
                <v-expand-transition>
                  <div v-if="hover" 
                    class="d-flex transition-fast-in-fast-out orange darken-1 v-card--reveal display-3 white--text text-outline" 
                    style="height: 100%; opacity:0.9">
                      &euro; {{product.price}}
                  </div>
                </v-expand-transition>
              </v-img>
              <v-card-text class="pt-4" style="position: relative;">
                <v-btn absolute color="orange" class="white--text" fab medium right top>
                  <v-icon>mdi-cart</v-icon>
                </v-btn>
                <div class="font-weight-light grey--text title mb-2">{{product.category}}</div>
                  <h3 class="headline font-weight-light orange--text mb-2">{{product.title}}</h3>
                  <div class="font-weight-light title mb-2">{{product.description}}
                </div>
              </v-card-text>
            </v-card>
          </v-hover>
        </v-flex>
      </template>
    </v-layout>
  </v-container>
</template>

<script>
  export default {
    data() {
      return {
        products:[
          {
            price: 14.99,
            src: 'https://cdn.vuetifyjs.com/images/cards/kitchen.png',
            category: 'For the perfect meal',
            title: 'QW cooking utensils',
            description: 'Our Vintage kitchen utensils delight any chef.\n Made of bamboo by hand'
          },
          {
            price: 33.99,
            src: 'https://cdn.vuetifyjs.com/images/cards/kitchen.png',
            category: 'For the perfect meal',
            title: 'QW cooking utensils',
            description: 'Our Vintage kitchen utensils delight any chef.\n Made of bamboo by hand'
          },
          {
            price: 24.99,
            src: 'https://cdn.vuetifyjs.com/images/cards/kitchen.png',
            category: 'For the perfect meal',
            title: 'QW cooking utensils',
            description: 'Our Vintage kitchen utensils delight any chef.\n Made of bamboo by hand'
          },
          {
            price: 14.99,
            src: 'https://cdn.vuetifyjs.com/images/cards/kitchen.png',
            category: 'For the perfect meal',
            title: 'QW cooking utensils',
            description: 'Our Vintage kitchen utensils delight any chef.\n Made of bamboo by hand'
          },
          {
            price: 4.99,
            src: 'https://cdn.vuetifyjs.com/images/cards/kitchen.png',
            category: 'For the perfect meal',
            title: 'QW cooking utensils',
            description: 'Our Vintage kitchen utensils delight any chef.\n Made of bamboo by hand'
          },
          {
            price: 17.99,
            src: 'https://cdn.vuetifyjs.com/images/cards/kitchen.png',
            category: 'For the perfect meal',
            title: 'QW cooking utensils',
            description: 'Our Vintage kitchen utensils delight any chef.\n Made of bamboo by hand'
          },
        ]
      }
    },
  }
</script>

<style scoped>
  .v-card--reveal{
    align-items: center;
    bottom: 0;
    justify-content: center;
    opacity: 0.7;
    position: absolute;
    width: 100%;
  }
  .text-outline{
    text-shadow: -1px 0 gray, 0 1px gray, 1px 0 gray, 0 -1px gray;
  }
</style>

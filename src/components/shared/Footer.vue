<template>
  <v-footer dark height="auto">
    <v-card flat tile class="indigo lighten-1 white--text text-xs-center flex">
      <v-card-text>
        <v-btn v-for="icon in icons" :key="icon" clas="mx-3" dark icon>
          <v-icon size="24px">  {{icon}} </v-icon>
        </v-btn>
      </v-card-text>
      <v-card-text>
        Shoppingcart footer text here
      </v-card-text>
      <v-divider></v-divider>
      <v-card-text class="white--text text-center">
        &copy; {{year}} - <strong>Heltson.com</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
  export default {
    data() {
      return {
        icons: [
            'mdi-facebook-box',
            'mdi-twitter-box',
            'mdi-google-plus-box',
            'mdi-linkedin-box',
            'mdi-instagram'
        ],
        year: new Date().getFullYear()
      }
    }
  }
</script>

<style lang="scss" scoped>

</style>
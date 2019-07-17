<template>
  
    <div>
      <v-navigation-drawer v-model="drawer" app temporary>
        <v-list>
          <v-list-tile>
            <v-list-tile-content>
              <v-list-tile-title>
                Menu
              </v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>
          <v-divider></v-divider>

          <template v-for="(item, index) in items">
            <v-list-tile :key="index" :href="item.href" >
              <v-list-tile-action>
                <v-icon light v-html="item.icon"></v-icon>
              </V-list-tile-action>
              <v-list-tile-action>
                <v-list-tile-title v-html="item.title"></v-list-tile-title>
              </v-list-tile-action>
            </v-list-tile>
          </template>
        </v-list>
      </v-navigation-drawer>
      
      <v-toolbar dark>
        <v-toolbar-side-icon v-on:click="drawer = !drawer"></v-toolbar-side-icon>
        <v-toolbar-title ><router-link to="/">ShoppingCart</router-link></v-toolbar-title>
        <v-spacer></v-spacer>

        <v-toolbar-items>
          <v-btn flat>
            Products
          </v-btn>
          <v-btn flat class="ml-4" to="/basket">

            <!-- <a href="/basket">  -->
            <v-badge left color="green" class="px-2">
              <span slot="badge" >5</span>
              <v-icon>mdi-cart</v-icon>Basket
            </v-badge>
            <!-- </a>  -->
          </v-btn>
        </v-toolbar-items>
      </v-toolbar>
    </div>
 
</template>

<script>
  export default {
    data() {
      return {
        drawer: false,
        items: [{
          icon: 'perm_identity',
          href: '#',
          title: 'Account'
        }]
      }
    }
  }
</script>

<style  scoped>
a {
  color: white;
  text-decoration: none;
}
</style>
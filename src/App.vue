<template>
  <v-app style="background-color: #f1f1f1">
    <v-app-bar
      app
      fade-img-on-scroll
      flat
      color="#fa880c"
      class="white--text"
      height="120px"
    >
      <div
        class="d-flex justify-space-between align-center"
        style="width: 100%; z-index: 5"
      >
        <h2>Easy Pick</h2>
        <div>
          <v-btn icon class="btn_cart"
            ><v-icon class="cart_icon">mdi-bell-ring</v-icon></v-btn
          >
          <v-btn icon class="btn_cart ml-3"
            ><v-icon class="cart_icon">mdi-cart</v-icon></v-btn
          >
        </div>
      </div>
    </v-app-bar>
    <v-main>
      <router-view></router-view>
    </v-main>
    <v-bottom-navigation app flat fixed style="z-index: 5">
      <v-btn value="recent">
        <span>Recent</span>

        <v-icon>mdi-history</v-icon>
      </v-btn>

      <v-btn value="favorites">
        <span>Favorites</span>

        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn value="nearby">
        <span>Nearby</span>

        <v-icon>mdi-map-marker</v-icon>
      </v-btn>
    </v-bottom-navigation>
  </v-app>
</template>

<script>
export default {
  name: "App",
  data: () => ({}),
};
</script>
<style>
* {
  padding: 0;
  margin: 0;
}
html::-webkit-scrollbar,
body::-webkit-scrollbar,
main::-webkit-scrollbar {
    display: none;
    width: 0;
    -ms-overflow-style: none;
}

.normal_size_font{
  font-size:0.9em;
}
.btn_cart {
  border-radius: 50%;
  background-color: white;
  color: #fa880c;
  width: 40px!important;
  height: 40px!important;
}
.btn_cart .cart_icon {
  color: #fa880c !important;
}
.container {
  max-width: 1366px;
  height: 100vh;
  margin: 0 auto;
}
.lt-sp-1 {
  letter-spacing: 1px;
}
</style>

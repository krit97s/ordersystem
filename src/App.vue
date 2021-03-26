<template>
  <v-app style="background-color: #f1f1f1">
    <v-app-bar
      app
      hide-on-scroll
      color="#fa880c"
      class="white--text d-flex flex-column justify-center"
      height="130px"
    >
      <div style="width: 100%; z-index: 5">
        <!-- <h2>Easy Pick</h2> -->
        <div class="d-flex justify-end mt-3">
          <v-btn icon class="btn_cart"
            ><v-icon class="cart_icon">mdi-bell-ring-outline</v-icon></v-btn
          >
          <v-btn icon class="btn_cart ml-3"
            ><v-icon class="cart_icon">mdi-cart-outline</v-icon></v-btn
          >
        </div>
        <div @click="onSearch()">
          <v-text-field
            disabled
            dense
            solo
            color="#fa880c"
            class="mt-3"
            flat
            label="ค้นหารายการที่คุณสนใจ"
            prepend-inner-icon="mdi-magnify"
          ></v-text-field>
        </div>
      </div>
    </v-app-bar>
    <v-main>
      <searchProduct
        :productItem="catagoryItem"
        :dialogSearch="dialogSearch"
        @closeserachDialog="closeserachDialog"
      />
      <router-view></router-view>
    </v-main>
    <v-bottom-navigation
      app
      flat
      fixed
      hide-on-scroll
      style="z-index: 5"
      active-class="active_class_menu"
    >
      <v-btn value="home">
        <span>หน้าแรก</span>

        <v-icon>mdi-home-outline</v-icon>
      </v-btn>

      <v-btn value="history">
        <span>รายการ</span>

        <v-icon>mdi-cart-outline</v-icon>
      </v-btn>

      <v-btn value="news">
        <span>ข่าวสาร</span>

        <v-icon>mdi-newspaper-variant-outline</v-icon>
      </v-btn>
      <v-btn value="settings">
        <span>ตั้งค่า</span>

        <v-icon>mdi-cog-outline</v-icon>
      </v-btn>
    </v-bottom-navigation>
  </v-app>
</template>

<script>
import searchProduct from "@/components/product/searchProduct";
export default {
  name: "App",
  components: {
    searchProduct,
  },
  data: () => ({
    catagoryItem: [
      {
        icon: "mdi-food-drumstick",
        title: "Meat",
      },
      {
        icon: "mdi-beer",
        title: "Drink",
      },
      {
        icon: "mdi-fruit-cherries",
        title: "Vegetable",
      },
      {
        icon: "mdi-shaker",
        title: "Sushi",
      },
      {
        icon: "mdi-ice-cream",
        title: "Desert",
      },
      {
        icon: "mdi-food-turkey",
        title: "Fast food",
      },
    ],
    dialogSearch: false,
  }),
  methods: {
    closeserachDialog() {
      this.dialogSearch = false;
    },
    onSearch() {
      this.dialogSearch = true;
    },
  },
};
</script>
<style>
@import url("https://fonts.googleapis.com/css2?family=Kanit:wght@300;400;500;700&display=swap");
* {
  padding: 0;
  margin: 0;
  font-family: "Kanit", sans-serif;
}
html::-webkit-scrollbar,
body::-webkit-scrollbar,
main::-webkit-scrollbar {
  display: none;
  width: 0;
  -ms-overflow-style: none;
}

.normal_size_font {
  font-size: 0.9em;
  font-weight: 400;
}
.btn_cart {
  border-radius: 50%;
  background-color: white;
  color: #fa880c;
  width: 35px !important;
  height: 35px !important;
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
.active_class_menu {
  color: #fa880c !important;
}
</style>

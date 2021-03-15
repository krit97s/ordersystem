<template>
  <div class="home">
    <v-row no-gutters class="product_panel">
      <v-col cols="12">
        <Swipper/>
      </v-col>
    </v-row>
    <v-row no-gutters justify="center" class="pa-3 catagory_panel">
      <v-col cols="12">
        <div class="lt-sp-1"><b>หมวดหมู่อาหาร</b></div>
      </v-col>
      <v-col cols="4" v-for="(item, index) in catagoryItem" :key="index">
        <CatagoryItem :catagoryItem="item" />
      </v-col>
    </v-row>
    <v-row no-gutters class="pa-3 product_panel">
      <div class="lt-sp-1"><b>รายการอาหาร</b></div>
      <v-col
        cols="12"
        class="mt-2"
        v-for="(item, index) in catagoryItem"
        :key="index"
      >
        <ProductItem :catagoryItem="item" />
      </v-col>
    </v-row>
  </div>
</template>

<script>
// @ is an alias to /src
import CatagoryItem from "@/components/catagory/catagoryItem";
import ProductItem from "@/components/product/productItem";
import Swipper from "@/components/swiper/swiper";
export default {
  components: {
    CatagoryItem,
    ProductItem,
    Swipper
  },
  data() {
    return {
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
    };
  },
  name: "Home",
};
</script>

<style scoped>
.product_panel {
  background: white;
  width: 100%;
}
.catagory_panel {
  background: white;
  border-bottom-right-radius: 10px;
  border-bottom-left-radius: 10px;
  width: 100%;
}
</style>

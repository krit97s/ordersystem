<template>
  <div>
    <v-dialog
      v-model="dialogSearch"
      fullscreen
      persistent
      transition="dialog-bottom-transition"
    >
      <v-card style="border-radius: 0px !important">
        <v-row justify="center" no-gutters>
          <v-col
            cols="12"
            class="d-flex align-center justify-space-between mt-2"
          >
            <v-btn icon @click="$emit('closeserachDialog')">
              <v-icon>mdi-arrow-left</v-icon>
            </v-btn>
          </v-col>
          <v-col cols="12" class="pl-3 pr-3 mt-2">
            <v-text-field
              dense
              color="#fa880c"
              label="ค้นหารายการที่คุณสนใจ"
              solo
              prepend-inner-icon="mdi-magnify"
            ></v-text-field>
          </v-col>
        </v-row>
        <v-row no-gutters class="pl-3 pr-3" style="margin-top: -10px">
          <div class="lt-sp-1"><b>ค้นหารายการที่คุณสนใจ</b></div>
          <v-col
            cols="12"
            class="mt-2"
            v-for="(item, index) in productItem"
            :key="index"
          >
            <ProductItem :eachproductItem="item" />
          </v-col>
        </v-row>
      </v-card>
    </v-dialog>
  </div>
</template>
<script>
import ProductItem from "@/components/product/productItem";
export default {
  components: {
    ProductItem,
  },
  computed: {
    // filterProduct() {
    //     return this.
    // },
  },
  props: ["dialogSearch", "productItem"],
};
</script>
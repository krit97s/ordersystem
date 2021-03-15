<template>
  <div
    class="catagory_item d-flex justify-center flex-column align-center pt-4"
  >
    <v-btn icon class="btn_catagory"
      ><v-icon class="white--text">{{ catagoryItem.icon }}</v-icon></v-btn
    >
    <div class="lt-sp-1 normal_size_font">{{ catagoryItem.title }}</div>
  </div>
</template>

<script>
// @ is an alias to /src
export default {
  props: ["catagoryItem"],
  name: "catagoryItem",
};
</script>

<style scoped>
.btn_catagory {
  border-radius: 50%;
  background-color: #fa880c;
  color: white;
  width: 50px!important;
  height: 50px!important;
}
.catagory_panel {
  background: white;
  border-bottom-right-radius: 10px;
  border-bottom-left-radius: 10px;
  position: absolute;
  width: 100%;
  z-index: 1;
}
</style>

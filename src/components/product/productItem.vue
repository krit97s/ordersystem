<template>
  <div>
    <v-row>
      <v-col cols="5"
        ><v-img
          src="http://c.files.bbci.co.uk/8F5F/production/_109030763_gettyimages-687790334.jpg"
          cover
          width="100%"
          height="100%"
          style="border-radius: 3px"
        ></v-img
      ></v-col>
      <v-col cols="7" class="normal_size_font"
        ><div class="d-flex justify-space-between" style="font-weight: 500">
          <div>เนื้อ A4</div>
          <div>฿ 50</div>
        </div>
        <div style="color: grey; font-weight: 300">
          เนื้อคุณภาพสูงสุดมีไขมันมากที่สุด
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script>
// @ is an alias to /src
export default {
  props: ["eachproductItem"],
  name: "productItem",
};
</script>

<style scoped>
</style>

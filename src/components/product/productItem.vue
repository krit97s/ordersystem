<template>
  <div>
    <v-row>
      <v-col cols="7"
        ><v-img
          src="http://c.files.bbci.co.uk/8F5F/production/_109030763_gettyimages-687790334.jpg"
          cover
          width="100%"
          height="100%"
          style="border-radius: 3px"
        ></v-img
      ></v-col>
      <v-col cols="5" class="normal_size_font d-flex justify-space-between"
        ><div>เนื้อ A4</div>
        <div>50 บาท</div></v-col
      >
    </v-row>
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
</style>

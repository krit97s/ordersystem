<template>
  <div>
    <swiper ref="mySwiper" class="swiper" :options="swiperOption">
      <swiper-slide
        ><v-img
          src="https://miro.medium.com/max/4000/1*l0zjZEkNxQZeWl9ovxfKiw.jpeg"
          width="100%"
          :aspect-ratio="16 / 9"
        ></v-img
      ></swiper-slide>
      <swiper-slide
        ><v-img
          src="https://s3.ap-southeast-1.amazonaws.com/asset.punpro.com/cover-contents/i7861/1581911304587-Shibuya-Shab-2_0.png"
          width="100%"
          :aspect-ratio="16 / 9"
        ></v-img
      ></swiper-slide>
      <swiper-slide
        ><v-img
          src="http://blog.hungryhub.com/wp-content/uploads/2020/08/%E0%B8%9B%E0%B8%B4%E0%B9%89%E0%B8%87%E0%B8%A2%E0%B9%88%E0%B8%B2%E0%B8%87-%E0%B8%8A%E0%B8%B2%E0%B8%9A%E0%B8%B9-cover.jpg"
          width="100%"
          :aspect-ratio="16 / 9"
        ></v-img
      ></swiper-slide>

         <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
export default {
  data() {
    return {
      swiperOption: {
        swiperOption: {
          slidesPerView: 'auto',
          pagination: {
            el: '.swiper-pagination',
            dynamicBullets: true
          }
        },
      },
    };
  },
};
</script>
<style lang="scss" scoped>
.swiper-slide {
  width: 80%;
}
.swiper-slide:nth-child(2n) {
  width: 60%;
}
.swiper-slide:nth-child(3n) {
  width: 40%;
}
</style>

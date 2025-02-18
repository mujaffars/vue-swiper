<template>
  <div class="swiper-container">
    <swiper
      :modules="[Pagination, Navigation]"
      :slides-per-view="1"
      :space-between="10"
      :pagination="{ clickable: true }"
      :navigation="true"
    >
      <swiper-slide v-for="(image, index) in images" :key="index">
        <img :src="image" alt="Slide Image" />
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';
import 'swiper/css/navigation';
import { Pagination, Navigation } from 'swiper/modules';

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    const images = [
      "https://picsum.photos/600/300?random=1",
      "https://picsum.photos/600/300?random=2",
      "https://picsum.photos/600/300?random=3",
    ];

    return {
      images,
      Pagination,
      Navigation,
    };
  },
};
</script>

<style scoped>
.swiper-container {
  width: 100%;
  max-width: 600px;
  margin: auto;
}
img {
  width: 100%;
  border-radius: 10px;
}
</style>

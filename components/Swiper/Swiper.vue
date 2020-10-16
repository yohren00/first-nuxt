<template>
  <div class="swiper-container">
    <div class="swiper-wrapper">
      <div class="swiper-slide" v-for="(item,index) in slide" :key="index">{{item}}</div>
    </div>
    <!-- Add Arrows -->
    <div class="swiper-button-next"></div>
    <div class="swiper-button-prev"></div>
    <!-- Add Pagination -->
    <div class="swiper-pagination"></div>
  </div>
</template>


<script>
import Swiper from "swiper/bundle";
import "swiper/swiper-bundle.css";

export default {
  data() {
    return {
      slide: ["React", "Vue", "Angular"],
    };
  },
  mounted() {
    new Swiper(".swiper-container", {
      //循環播放
      loop: true,
      //導航設定（上一頁、下一頁）
      autoplay: {
        delay: 5000,
        disableOnInteraction: false,
      },
      navigation: {
        nextEl: ".swiper-button-next",
        prevEl: ".swiper-button-prev",
      },
      //分頁設定
      pagination: {
        el: ".swiper-pagination",
      },
      //滾輪控制
      mousewheel: false,
      //鍵盤控制
      keyboard: true,
    });
  },
};
</script>

<style scoped>
.swiper-container {
  width: 100%;
  height: 100%;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: #fff;

  display: -webkit-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  -webkit-justify-content: center;
  justify-content: center;
  -webkit-box-align: center;
  -ms-flex-align: center;
  -webkit-align-items: center;
  align-items: center;
}
</style>

<template>
  <div class="banner">
    
    <swiper :options="swiperOption" class="w">
        <!-- <div class="parallax-bg" slot="parallax-bg" data-swiper-parallax="-23%"></div> -->
        <swiper-slide v-for="(item,index) in swiperData" :key="index">
          <div class="title" data-swiper-parallax="-100">{{item.title}}</div>
          <div class="subtitle" data-swiper-parallax="-200">{{item.info}}</div>
          <div class="text" data-swiper-parallax="-300">
            {{item.info}}
          </div>
        </swiper-slide>
        <div class="swiper-pagination swiper-pagination-white" slot="pagination"></div>
        <div class="swiper-button-prev swiper-button-black hidden-xs-only" slot="button-prev"></div>
        <div class="swiper-button-next swiper-button-black hidden-xs-only" slot="button-next"></div>
      </swiper>
  </div>
</template>
<script>
import "swiper/dist/css/swiper.css";
import { swiper, swiperSlide } from "vue-awesome-swiper";
export default {
  data() {
    return {
      swiperData: [
        { title: "生活", info: "爱生活 艳阳天", view: "view port", imgSrc: "" },
        { title: "生活", info: "爱生活 艳阳天", view: "view port", imgSrc: "" },
        { title: "生活", info: "爱生活 艳阳天", view: "view port", imgSrc: "" }
      ],
      swiperOption: {
        // some swiper options/callbacks
        // 所有的参数同 swiper 官方 api 参数
        // ...
        speed: 600,
        parallax: true,
        pagination: {
          el: ".swiper-pagination",
          clickable: true
        },
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev"
        }
      }
    };
  },
  components: {
    swiper,
    swiperSlide
  }
};
</script>
<style lang="scss" scoped>
.swiper-slide {
  font-size: 18px;
  color: #333;
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
  padding: 40px 60px;
  height: calc( 100vw / 4);
  min-height: 300px;
  background-color: transparent ;
  justify-content: space-around ;
}
.swiper-slide .title {
  font-size: 41px;
  font-weight: 300;
}
.swiper-slide .subtitle {
  font-size: 21px;
}
.swiper-slide .text {
  font-size: 14px;
  max-width: 400px;
  line-height: 1.3;
}
.swiper-container{
    z-index: -1;
}
</style>

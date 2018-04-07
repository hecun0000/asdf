<template>
  <div class="banner">
    
    <swiper :options="swiperOption" class="wbanner">
        <!-- <div class="parallax-bg" slot="parallax-bg" data-swiper-parallax="-23%"></div> -->
        <swiper-slide v-for="(item,index) in swiperData" :key="index" class="banner" :class="item.class">
            <img :src="item.imgSrc" alt="">
            <div class="info" >
                <div class="title" data-swiper-parallax="-200">{{item.title}}</div>
                <div class="subtitle" data-swiper-parallax="-300">{{item.info}}</div>
                <div class="text" data-swiper-parallax="-400">{{item.info}}</div>
            </div>
        </swiper-slide>
        <div class="swiper-pagination swiper-pagination-white" slot="pagination"></div>
        <div class="banner-button banner-prev hidden-xs-only" slot="button-prev">←</div>
        <div class="banner-button banner-next hidden-xs-only" slot="button-next">→</div>
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
        {
          title: "生活方式",
          info: "爱生活 艳阳天",
          view: "view port",
          imgSrc: require("../assets/img/banner/1.jpg"),
          class: "banner-center"
        },
        {
          title: "生活",
          info: "爱生活 艳阳天",
          view: "view port",
          imgSrc: require("../assets/img/banner/2.png"),
          class: "banner-left"
        },
        {
          title: "生活",
          info: "爱生活 艳阳天",
          view: "view port",
          imgSrc: require("../assets/img/banner/3.jpg"),
          class: "banner-left"
        },
        {
          title: "生活",
          info: "爱生活 艳阳天",
          view: "view port",
          imgSrc: require("../assets/img/banner/4.png"),
          class: "banner-left"
        }
      ],
      swiperOption: {
        speed: 600,
        parallax: true,
        grabCursor: true,
        pagination: {
          el: ".swiper-pagination",
          clickable: true
        },
        loop: true,
        autoplay: {
          delay: 2000,
          disableOnInteraction: true
        },

        navigation: {
          nextEl: ".banner-next",
          prevEl: ".banner-prev"
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
// 描述文字样式
.info {
  position: absolute;
  z-index: 6;
}
.banner-center {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  color: #fff;
  cursor: pointer;
  .title {
    border: 2px solid #fff;
    display: inline-block;
    font-size: 16px;
    padding: 5px 15px;
    height: 25px;
    line-height: 13px;
    box-sizing: border-box;

    &:hover {
    }
  }

  .subtitle {
    font-size: 40px;
    margin: 10px 0;
  }
}

.wbanner {
  width: 100%;
  max-width: 1000px;
  margin: 0 auto;
  //   上下按钮隐藏与显示
  &:hover .banner-button {
    display: block;
  }
}
.banner {
  position: relative;
}

// 控制按钮
.banner-button {
  position: absolute;
  width: 30px;
  height: 30px;
  // display: block;
  top: 50%;
  margin-top: -15px;
  background: #fff;
  border: 2px solid #666;
  text-align: center;
  line-height: 25px;
  font-weight: 900;
  z-index: 4;
  cursor: pointer;
  display: none;
  &:hover {
    border: 3px solid #333;
  }
  &.banner-prev {
    left: 5px;
  }
  &.banner-next {
    right: 5px;
  }
}
</style>

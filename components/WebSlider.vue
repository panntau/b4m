<template>
  <section id="home" class="no-padding slider-style2 border-none">
          <!-- You can find this swiper instance object in current component by the "mySwiper"  -->
    <div v-swiper:mySwiper="swiperOption">
        <div class="swiper-wrapper">
          <!-- slider item -->
          <div class="swiper-slide" v-for="(item) in items" :key="item.id">
            <div class="owl-theme light-pagination xs-no-owl-buttons">
                <!-- slider item -->
                <div class="item owl-bg-img tz-builder-bg-image cover-background" data-img-size="(W)1920px X (H)994px" 
                style="background: linear-gradient(rgba(15, 15, 15, 0.75), rgba(15, 15, 15, 0.75)) repeat scroll 0% 0%, transparent repeat scroll 0% 0%;">
                    <img class="swiper-slide__bg" :src="item.bg" :alt="item.title">
                        <div class="container one-sixth-screen xs-one-second-screen position-relative">
                            <div class="col-md-7 col-sm-10 col-xs-12 margin-lr-auto slider-typography text-center">
                                <div class="slider-text-middle-main">
                                    <div class="slider-text-middle">
                                        <div class="title-extra-large-9 font-weight-700 text-dark-aqua margin-ten-bottom alt-font slider-title tz-text">
                                            {{item.title}}
                                        </div>
                                        <div class="text-extra-large text-light-gray font-weight-400 margin-twelve-bottom xs-margin-twenty-bottom slider-text xs-title-small tz-text width-85 xs-width-95 margin-lr-auto">
                                            <p>
                                                {{item.text}}
                                            </p>
                                        </div>
                                        <div class="btn-dual" >
                                            <a v-for="(value , key) in item.links" :key="value.id" class="btn btn-large xs-btn-small btn-border btn-circle text-blue-gray highlight-button-blgr-border propClone font-weight-300"
                                                :href="value">
                                                <span class="tz-text" id="tz-btn-1">
                                                    {{key}}
                                                </span>
                                            </a>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
            </div>
          </div>
        </div>
        <div class="swiper-pagination swiper-pagination-bullets"></div>
            
        <!-- If we need navigation buttons -->
        <div class="swiper-button-prev">
            <svg viewbox="0 0 60 100"><polygon points="10,50 50,10 50,90" class="triangle" />&lt;</svg>
        </div>
        <div class="swiper-button-next">
            <svg viewbox="0 0 60 100"><polygon points="10,10 10,90 50,50" class="triangle" />&gt;</svg>
        </div>
    </div>
        
        <!-- end slider item -->
  </section>
</template>

<script>
// import 'swiper/dist/css/swiper.css';
// import { swiper, swiperSlide } from 'vue-awesome-swiper';

export default {
  name: 'WebSlider',
  //   components: {
  //     swiper,
  //     swiperSlide
  //   },
  props: {
    items: {
      type: Array,
      required: true
    }
  },
  data() {
    return {
      swiperOption: {
        loop: true,
        slidesPerView: 'auto',
        centeredSlides: true,
        spaceBetween: 30,
        autoplay: {
          delay: 5000,
          disableOnInteraction: false
        },
        pagination: {
          el: '.swiper-pagination',
          clickable: true
        },
        navigation: {
          nextEl: '.owl-next',
          prevEl: '.owl-prev'
        },
        on: {
          slideChange() {
            console.log('onSlideChangeEnd', this);
          },
          tap() {
            console.log('onTap', this);
          }
        }
      }
    };
  },
  mounted() {
    console.log('app init', this);
    setTimeout(() => {
      this.banners.push('/5.jpg');
      console.log('banners update');
    }, 3000);
    console.log(
      'This is current swiper instance object',
      this.mySwiper,
      'I will slideTo banners 3'
    );
    this.mySwiper.slideTo(3);
  }
};
</script>
<style lang="scss">
// @import '@node_modules/tiny-slider/src/tiny-slider';
.my-swiper {
  height: 300px;
  width: 100%;
  .swiper-slide {
    text-align: center;
    font-size: 38px;
    font-weight: 700;
    background-color: #eee;
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
  }
  .swiper-pagination {
    > .swiper-pagination-bullet {
      background-color: red;
    }
  }
}
.swiper-slide__bg {
  position: absolute;
  top: 0;
  left: 0;
  //   transform: translateX(-50%);
  //   transform: translateY(-50%);
}
.triangle {
  fill: transparent;
  stroke: currentColor;
  stroke-width: 2;
  color: rgb(235, 36, 42);
}
.swiper-button {
  &-next,
  &-prev {
    background: none;
  }
}
</style>

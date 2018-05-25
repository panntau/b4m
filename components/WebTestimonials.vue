<template>
  <section id="title-section2" 
  class="cover-background tz-builder-bg-image padding-110px-tb border-none xs-padding-top-60px"
    data-img-size="(W)1920px X (H)573px">
      <div class="container position-relative" id="testimonials-section1">
        <div v-swiper:mySwiper="swiperOption">
        <div class="swiper-wrapper owl-slider-full owl-carousel owl-theme light-pagination owl-pagination-bottom xs-no-owl-buttons">
            <div class="swiper-slide" v-for="(item) in items" :key="item.id">
                <!-- testimonial item -->
                <div class="item">
                    <div class="col-md-6 col-sm-8 col-xs-12 center-col text-center">
                        <i class="tz-icon-color fa fa-quote-left text-deep-red title-extra-large margin-seven-bottom" id="tz-icon-1"></i>
                        <div class="text-medium text-medium-gray margin-five-bottom tz-text" id="tz-slider-text67">
                            {{item.text}}
                        </div>
                        <div class="text-white alt-font margin-seven-bottom display-block tz-text" id="tz-slider-text68">
                            <span class="testimonial__author">{{item.author}}</span>
                            <span class="testimonial__company" v-if="item.company"> - {{item.company}}</span>
                        </div>
                        <div class="separator-line bg-deep-red margin-lr-auto tz-background-color"></div>
                    </div>
                </div>
                <!-- end testimonial item -->
               
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
    </div>
  </section>
</template>

<script>
export default {
  name: 'WebTestimonials',
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

<style lang="sass" scoped>
.testimonial__author,
.testimonial__company,
    text-transform: uppercase

.cover-background
  background: linear-gradient(rgba(20, 20, 20, 0.95), rgba(20, 20, 20, 0.7)) repeat scroll 0% 0%, rgba(0, 0, 0, 0) url('~assets/images/bg-image/testimonials.jpg') repeat scroll 0% 0%
</style>

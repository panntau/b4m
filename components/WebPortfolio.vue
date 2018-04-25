<template>
  <section class="bg-white builder-bg padding-110px-tb xs-padding-60px-tb" id="portfolios-section3">
    <div class="container">
        <div class="row">
            <!-- section title -->
            <div class="col-md-12 col-sm-12 col-xs-12 text-center">
                <h2 class="section-title-large sm-section-title-medium xs-section-title-large text-dark-gray font-weight-600 alt-font margin-three-bottom xs-margin-fifteen-bottom tz-text"
                    id="tz-slider-text235">PORTFOLIO</h2>
                <div class="text-medium width-60 margin-lr-auto md-width-70 sm-width-100 tz-text margin-thirteen-bottom xs-margin-nineteen-bottom"
                    id="tz-slider-text236">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the
                    industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of
                    type and scrambled it to make a type specimen book.</div>
            </div>
            <!-- end section title -->
            <div class="col-md-12 col-sm-12 col-xs-12 margin-six-bottom xs-margin-twelve-bottom text-center">
                <!-- filter navigation -->
                <ul class="portfolio-filter nav nav-tabs tab-style3 border-none alt-font font-weight-500">
                    <li class="propClone active">
                        <a href="#" data-filter="*" id="tz-slider-text237" class="tz-text">Vše</a>
                    </li>
                    <li class="propClone">
                        <a href="#" data-filter=".brand" id="tz-slider-text238" class="tz-text">BRANDING</a>
                    </li>
                    <li class="propClone">
                        <a href="#" data-filter=".web" id="tz-slider-text239" class="tz-text">WEB</a>
                    </li>
                    <li class="propClone">
                        <a href="#" data-filter=".tisk" id="tz-slider-text240" class="tz-text">TISK</a>
                    </li>
                    <li class="propClone">
                        <a href="#" data-filter=".foto" id="tz-slider-text241" class="tz-text">FOTOGRAFIE</a>
                    </li>
                    <li class="propClone">
                        <a href="#" data-filter=".product" id="tz-slider-text242" class="tz-text">PRODUKT</a>
                    </li>
                </ul>
                <!-- end filter navigation -->
            </div>
        </div>
    </div>
    <!-- end section title -->
    <div class="container-fluid">
        <div class="row">
            <div class="work-4col wide gutter">
                <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12">
                    <div class="grid-gallery">
                        <div class="tab-content">
                          <no-ssr>
                            <ul class="masonry-container grid work-gallery" v-masonry transition-duration="3s" item-selector=".item">
                              <li v-masonry-tile class="item brand xs-no-padding" :key="index" v-for="(item, index) in blocks">
                                <figure>
                                    <div class="gallery-img lightbox-gallery">
                                        <!-- <a :href="item.src" title=""> -->
                                            <img v-img:portfolio :src="item.src" id="tz-bg-96" :title="item.title" :alt="item.title">
                                        <!-- </a> -->
                                        <!-- <p>{{item.category}} - {{index}}</p> -->
                                    </div>
                                </figure>
                              </li>
                            </ul>
                          </no-ssr>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
  </section>
</template>

<script>
import NoSSR from 'vue-no-ssr';

export default {
  components: {
    'no-ssr': NoSSR
  },
  data() {
    return {
      blocks: [
        {
          src: 'images/portfolio/brand1.jpg',
          category: 'brand',
          title: 'Brand XY, logo and brand identity'
        },
        {
          src: 'images/portfolio/brand2.jpg',
          category: 'brand'
        },
        {
          src: 'images/portfolio/brand3.jpg',
          category: 'brand'
        },
        {
          src: 'images/portfolio/brand4.jpg',
          category: 'brand'
        },
        {
          src: 'images/portfolio/product7.jpg',
          category: 'product'
        },
        {
          src: 'images/portfolio/product6.jpg',
          category: 'product'
        },
        {
          src: 'images/portfolio/product5.jpg',
          category: 'product'
        },
        {
          src: 'images/portfolio/product4.jpg',
          category: 'product'
        },
        {
          src: 'images/portfolio/product3.jpg',
          category: 'product'
        },
        {
          src: 'images/portfolio/product2.jpg',
          category: 'product'
        },
        {
          src: 'images/portfolio/product1.jpg',
          category: 'product'
        },
        {
          src: 'images/portfolio/web1.png',
          category: 'web'
        },
        {
          src: 'images/portfolio/web2.jpg',
          category: 'web'
        },
        {
          src: 'images/portfolio/web3.jpg',
          category: 'web'
        },
        {
          src: 'images/portfolio/web4.jpg',
          category: 'web'
        },
        {
          src: 'images/portfolio/foto1.jpeg',
          category: 'foto'
        },
        {
          src: 'images/portfolio/foto2.jpg',
          category: 'foto'
        },
        {
          src: 'images/portfolio/tisk1.jpg',
          category: 'tisk'
        },
        {
          src: 'images/portfolio/tisk2.jpg',
          category: 'tisk'
        },
        {
          src: 'images/portfolio/tisk3.jpg',
          category: 'tisk'
        },
        {
          src: 'images/portfolio/tisk4.jpg',
          category: 'tisk'
        },
        {
          src: 'images/portfolio/tisk5.jpg',
          category: 'tisk'
        }
      ]
    };
  },
  mounted() {
    if (typeof this.$redrawVueMasonry === 'function') {
      this.$redrawVueMasonry();
    }
  },
  methods:{
    
  }
};
</script>

<style lang="sass"  >
.masonry-container
  width: 100%
  display: inline-block
.work-4col 
  width: 100%
  
</style>
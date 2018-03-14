<template>
    <div>
      <web-header/>
      <web-slider></web-slider>
      <web-about/>
      <web-services/>
      <web-portfolio/>
      <web-testimonials/>
      <web-c-t-a/>
      <web-clients/>
      <web-contacts/>
      <web-map/>
      <web-footer/>
    </div>
</template>

<script>
import WebHeader from '~/components/WebHeader.vue';
import WebSlider from '~/components/Webslider.vue';
import WebAbout from '~/components/WebAbout.vue';
import WebServices from '~/components/WebServices.vue';
import WebPortfolio from '~/components/WebPortfolio.vue';
import WebTestimonials from '~/components/WebTestimonials.vue';
import WebCTA from '~/components/WebCTA.vue';
import WebClients from '~/components/WebClients.vue';
import WebContacts from '~/components/WebContacts.vue';
import WebMap from '~/components/WebMap.vue';
import WebFooter from '~/components/WebFooter.vue';
export default {
  components: {
    WebHeader,
    WebSlider,
    WebAbout,
    WebServices,
    WebPortfolio,
    WebTestimonials,
    WebCTA,
    WebClients,
    WebContacts,
    WebMap,
    WebFooter
  }
};
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto,
    'Helvetica Neue', Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}
.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}
.links {
  padding-top: 15px;
}
</style>

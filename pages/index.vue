<template>
    <div>
      <web-header/>
      <web-slider :items="loadedSliders" ></web-slider>
      <web-about/>
      <web-services/>
      <web-portfolio/>
      <web-testimonials :items="loadedTestimonials"/>
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
  },
  asyncData(context, callback) {
    setTimeout(() => {
      callback(null, {
        loadedSliders: [
          {
            title: 'Kreativní Agentura',
            text:
              "Lorem Ipsum is simply dummy text of the typesetting industry. Lorem Ipsum has been industry's standard dummy text.",
            bg: 'http://www.placecage.com/1920/1300', //'~assets/images/bg-image/woman-hand-pen-girl.jpg',
            links: {
              VÍCE: '#content-section39',
              PORTFOLIO: '#portfolios-section3'
            }
          },
          {
            title: 'Hmatatelné výsledky',
            text:
              "Lorem Ipsum is simply dummy text of the typesetting industry. Lorem Ipsum has been industry's standard dummy text.",
            bg: '~/assets/images/bg-image/pexels-photo-265087.jpeg',
            links: {
              VÍCE: '#content-section39',
              PORTFOLIO: '#portfolios-section3'
            }
          },
          {
            title: 'Precizní strategie',
            text:
              "Lorem Ipsum is simply dummy text of the typesetting industry. Lorem Ipsum has been industry's standard dummy text.",
            bg: '~assets/images/bg-image/marketing-board-strategy.jpg',
            links: {
              VÍCE: '#content-section39',
              PORTFOLIO: '#portfolios-section3'
            }
          }
        ],
        loadedTestimonials: [
          {
            text:
              "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the when an unknown printer took a galley of type scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting.",
            author: 'JOHN CARMACK',
            company: 'GOOGLE'
          },
          {
            text:
              "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the when an unknown printer took a galley of type scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting.",
            author: 'Jeremy Girard',
            company: 'Microsoft'
          },
          {
            text:
              "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the when an unknown printer took a galley of type scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting.",
            author: 'Paul Scrivens',
            company: 'Facebook'
          },
          {
            text: 'Ambition is a dream with a V8 engine.',
            author: 'Elvis'
          }
        ]
      });
    }, 1500);
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

<template>
  <q-page>
    <div class="row carousel-row">
      <div class="col-12">
        <q-carousel
          animated
          autoplay
          class="full-height"
          infinite
          navigation
          v-model="slide"
        >
          <q-carousel-slide :name="1" img-src="~assets/carousel/1.jpg">
            <div class="absolute-center custom-caption text-center q-ma-xl ">
              <div class="text-h2 text-white">October 1st an 2nd, 2020</div>
              <div class="text-h5 text-white">Two awsome days full of talks, workshops and discussions</div>
            </div>
          </q-carousel-slide>
          <q-carousel-slide :name="2" img-src="~assets/carousel/2.jpg">
            <div class="absolute-center custom-caption text-center q-ma-xl ">
              <div class="text-h2 text-white">Virtually everywhere</div>
              <div class="text-h5 text-white">You stay safe. We deliver an awesome conference experience to you.</div>
            </div>
          </q-carousel-slide>
          <q-carousel-slide :name="3" img-src="~assets/carousel/3.jpg">
            <div class="absolute-center custom-caption text-center q-ma-xl ">
              <div class="text-h2 text-white">High-rated speakers from all around the globe</div>
              <div class="text-h5 text-white">Ample time to meet and discuss with experts and other attendees</div>
            </div>
          </q-carousel-slide>
        </q-carousel>
      </div>
    </div>

    <div class="row q-my-none q-pb-xl bg-white">
      <div class="col-3 q-pa-md text-center">
        <q-avatar class="q-pa-xs q-ma-xs" size="15rem" text-color="primary" icon="campaign"/>
        <div class="text-h2">10+</div>
        <div class="text-h4">sessions</div>
      </div>
      <div class="col-3 q-pa-md text-center">
        <q-avatar class="q-pa-xs q-ma-xs" size="15rem" text-color="primary" icon="code"/>
        <div class="text-h2">4</div>
        <div class="text-h4">workshops</div>
      </div>
      <div class="col-3 q-pa-md text-center">
        <q-avatar class="q-pa-xs q-ma-xs" size="15rem" text-color="primary" icon="person"/>
        <div class="text-h2">14</div>
        <div class="text-h4">speakers</div>
      </div>
      <div class="col-3 q-pa-md text-center">
        <q-avatar class="q-pa-xs q-ma-xs" size="15rem" text-color="primary" icon="people"/>
        <div class="text-h2">100+</div>
        <div class="text-h4">attendees</div>
      </div>
    </div>

    <div class="row q-my-none bg-dark">
      <div class="col-12 q-my-md text-center">
        <h3 class="text-white">What's in it for you?</h3>

        <div class="row q-mt-none">
          <div class="col-4 q-pa-md text-center">
            <q-card class="my-card">

              <q-card-section>
                <div class="text-h6">Amazing atmosphere</div>
              </q-card-section>

              <q-card-section class="q-pt-none">
                As we go virtual this year, we all will miss the badge lanyards, drinks and snacks.
                But who needs those if the spirit, enthusiasm and the energy remain intact?
                Let's prove we can have even greater time meting online.
              </q-card-section>
              <q-video
                src="https://www.youtube.com/embed/vlD7kqDDUIQ"
                :ratio="16/9"
                />
            </q-card>
          </div>

          <div class="col-4 q-pa-md text-center">
            <q-card class="my-card">

              <q-card-section>
                <div class="text-h6">High quality talks</div>
              </q-card-section>

              <q-card-section class="q-pt-none">
                But don't take our word for granted, check
                <a href="https://www.youtube.com/playlist?list=PL4O1nDpoa5KT681y6VfNAtAtFbNo6Ikkr">last year's talks</a> out
                and be sure this year we'll raise the bar even higher.

                Don't have the time to watch them all and don't know which one to pick?
                May we suggest the "The Gordian Knot" keynote given by Alberto Brandolini.

              </q-card-section>

              <q-video
                src="https://www.youtube.com/embed/LDzU76oxaBE"
                :ratio="16/9"
                />
            </q-card>
          </div>

          <div class="col-4 q-pa-md text-center">
            <q-card class="my-card">

              <q-card-section>
                <div class="text-h6">Multi-device online platform</div>
              </q-card-section>

              <q-card-section class="q-pt-none">
                Something about what the online platform provides ...
              </q-card-section>

              <q-img
                src="https://expertshare-me.exactdn.com/wp-content/uploads/2020/06/header-Image1-1.png?strip=all&lossy=0&ssl=1"
                />
            </q-card>
          </div>
        </div>
      </div>
    </div>

    <div class="row q-my-none bg-grey-12">
      <div class="col-12 q-my-md text-center">
        <h3 class="text-grey-9">Registration</h3>

        <div class="row q-px-xl bg-grey-12">
          <div class="col-6 q-pa-md text-center">
            <div class="text-h5 text-uppercase">Blind bird tickets</div>
            <div>
            <q-avatar class="q-pa-xs q-ma-xs" size="10rem" text-color="grey-13">€35</q-avatar>
            </div>
            <div>
              <q-btn
                color="grey-13"
                disable
                label="Expired"
              />
            </div>
          </div>
          <div class="col-6 q-pa-md text-center">
            <div class="text-h5 text-uppercase">Regular tickets</div>
            <div>
            <q-avatar class="q-pa-xs q-ma-xs" size="10rem" text-color="primary">€95</q-avatar>
            </div>
            <div>
              <q-btn
                color="primary"
                label="Register now"
                size="xl"
                type="a"
                href="https://www.eventbrite.com/e/event-driven-microservices-conference-2020-by-axoniq-tickets-86501796201?aff=AxonIQ"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </q-page>
</template>

<style lang="sass" scoped>
  .custom-caption
    text-align: center
    padding: 12px
    color: white
    width: 100%
    background-color: rgba(0, 0, 0, .4)
  .carousel-row
    margin-top: 0 !important;
    margin-bottom: 0 !important;
    height: 80vh !important;
</style>

<script>

import QCarouselSlide from 'quasar'

export default {
  components: [
    QCarouselSlide
  ],
  name: 'Home',
  data () {
    return {
      slide: 1
    }
  }
}
</script>

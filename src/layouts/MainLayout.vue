<template>
  <q-layout view="hHh lpR fff">

    <q-header reveal elevated class="bg-black text-white">
      <q-toolbar class="q-py-xl">
        <q-toolbar-title class="absolute-center">
          <vue-typed-js
            ref="type1"
            id="type1"
            :strings="['Domain-', 'Event-', 'Model-']"
            :typeSpeed="50"
            :loop="true"
            :cursorChar="'|'"
            :backDelay="3000"
            :fadeOut="true"
            class="inline"
            >
            <span>
              <span class="text-h4 conf-name-light typing"></span>
              <strong class="text-h2 conf-name">DRIVEN</strong>
            </span>
          </vue-typed-js>
          <vue-typed-js
            ref="type2"
            id="type2"
            :strings="['Design', '(micro)services', 'Development']"
            :typeSpeed="50"
            :loop="true"
            :cursorChar="'|'"
            :backDelay="2500"
            :fadeOut="true"
            class="inline"
            :startDelay="1000"
            >
            <span>
              <span class="text-h4 conf-name-light typing"></span>
              <strong class="text-h3 conf-name-light">Conference</strong>
            </span>
          </vue-typed-js>
        </q-toolbar-title>
      </q-toolbar>
      <q-toolbar class="bg-primary">
        <div class="absolute-center">
          <q-btn
            v-for="page in pages"
            v-bind:key="page.name"
            flat
            :label="page.name"
            :to="{name: page.name}"
            />
        </div>

      </q-toolbar>
    </q-header>

    <q-page-container class="window-heigh">
      <router-view />
    </q-page-container>

    <q-footer elevated class="bg-grey-8 text-white">
      <q-toolbar class="row q-my-xl">
        <div class="col-3">
          <q-list dense flat padding>
            <q-item
              v-for="page in pages"
              v-bind:key="page.name"
              v-ripple
              manual-focus
              :active="true"
              :to="{name: page.name}"
              class="text-white"
            >
              <q-item-section>
                {{ page.name }}
              </q-item-section>
            </q-item>
          </q-list>
        </div>

        <q-separator vertical color='grey-12' spaced='3rem' />

        <div class="col-3">
          Organized by
          <q-img src="~assets/axoniq-logo-white.svg" width="10rem" class="q-ml-sm"></q-img>
        </div>

      </q-toolbar>
    </q-footer>

  </q-layout>
</template>

<style lang="scss" scoped>
  @import url('https://fonts.googleapis.com/css2?family=Nunito:wght@900&display=swap');
  @import url('https://fonts.googleapis.com/css2?family=Dosis:wght@200&display=swap');

  .conf-name {
    font-size: 3rem;
    letter-spacing: 0.5rem;
    font-family: 'Nunito', sans-serif;
  }

  .conf-name-light {
    font-family: 'Dosis', sans-serif;
  }

  .conf-headline {
    font-size: .7rem;
    position: relative;
    top: -1rem;
    text-align: justify;
    letter-spacing: 2px;
  }

  .inline {
    display: inline;
  }

</style>

<script>

import { VueTypedJs } from 'vue-typed-js'

export default {
  components: {
    VueTypedJs
  },
  computed: {
    pages: function () {
      return this.$router.options.routes
        .find(r => { return r.path === '/' })
        .children
    }
  },
  data () {
    return {
    }
  },
  methods: {
    pause (pos, typer) {
      // console.log(pos)
      // this.$refs.type2.strings = ['test1', 'test2', 'test3']
    }
  },
  mounted () {
  }

}
</script>

<template>
  <q-layout view="hHh lpR fff">

    <q-header reveal elevated class="bg-primary text-white">
      <q-toolbar class="q-py-lg">
        <q-toolbar-title>
          <strong class="text-h4">Event-driven Microservices</strong>
          <div><small class="q-mx-md">a <code>virtual</code> conference brought to you by AxonIQ</small></div>
        </q-toolbar-title>

        <q-space />

        <q-btn
          v-for="page in pages"
          v-bind:key="page.name"
          flat
          :label="page.name"
          :to="{name: page.name}"
          />

        <q-space />

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
              active="true"
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

<script>
export default {
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
  }
}
</script>

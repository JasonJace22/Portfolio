
<template>
  <q-layout view="hhh lpR fff">

    <q-header reveal elevated class="bg-primary text-black">
    <q-toolbar>
      <q-btn flat label="Homepage" />
      <q-space />
      <!--
        notice shrink property since we are placing it
        as child of QToolbar
      -->
<q-item clickable v-ripple @click="instagram('http://www.instagram.de')">
      <q-item-section side class="q-pa-xs">
        <q-avatar rounded size="25px">
          <img src="statics/instagram-logo.png" />
        </q-avatar>
      </q-item-section>
      <q-item-section>
        <q-item-label>Instagram</q-item-label>
      </q-item-section>
    </q-item>
          <!-- ENDE HEADER -->
    </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>

    <q-footer reveal elevated class="bg-grey-8 text-black">
      <q-toolbar>
        <q-toolbar-title>
          <q-avatar>
            <img src="https://cdn.quasar-framework.org/logo/svg/quasar-logo.svg">
          </q-avatar>
          Title
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>

  </q-layout>
</template>

<script>
import { openURL } from 'quasar'

export default {
  name: 'MyLayout',
  data () {
    return {
    }
  },
  methods: {
    openURL,
    instagram (thisURL) {
      openURL(thisURL)
    }
  }
}
</script>

<style>
</style>


<template>
  <q-layout view="hhh lpr fff">

    <q-header reveal elevated class="text-black">
    <q-toolbar>
      <q-btn flat label="LOGO: J" />
      <q-space />
   <!-- home -->
<q-btn class="underline" flat label="HOME" />
   <!-- more -->
<q-btn class="underline" flat label="ABOUT" />
   <!-- more -->
<q-btn class="underline" flat label="RESUME" />
   <!-- more -->
<q-btn class="underline" flat label="SKILLS" />
   <!-- more -->
<q-btn class="underline" flat label="KONTAKT" />
   <!-- more -->
          <!-- ENDE HEADER -->
    </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>

    <q-footer reveal elevated class="bg-primary text-black">
      <q-toolbar>
        <q-space />
   <!-- Github -->
      <q-item clickable v-ripple @click="github('http://www.github.de')">
      <q-item-section side class="q-pa-xs">
        <q-avatar rounded size="25px">
          <img src="../statics/github.png" />
        </q-avatar>
      </q-item-section>
      <q-item-section>
        <q-item-label>Github</q-item-label>
      </q-item-section>
    </q-item>
   <!-- instagram -->
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
      scrollPos: false
    }
  },
  methods: {
    openURL,
    instagram (thisURL) {
      openURL(thisURL)
    },
    github (thisURL) {
      openURL(thisURL)
    }
  }
}
</script>

<style>

.headerstyletop {
  background-color: #FFFFFF00;
  color: white !important;
}

.headerstyleNotTop {
  background-color: white;
  color: black !important;
}

.underline:after {
  content: ''; /* content ist leer... */
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0%;
  border-bottom: 2px solid darkcyan;
  transition: 0.5s;
}

.underline:hover:after {
  width: 100%;
}
</style>

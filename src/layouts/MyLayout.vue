
<template>
  <q-layout view="hHh lpR fFf" @scroll="onScroll">

    <q-header :class="{toptop : isTop, nottop : !isTop}">
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
<q-btn label="LOGIN" flat class="underline" @click="dialog = true" />
    <q-dialog v-model="dialog" transition-show="scale" transition-hide="scale">
      <q-card class="bg-blue text-white" style="width: 300px">
        <q-card-section>
          <div class="text-h6">LOGIN</div>
        </q-card-section>

        <q-card-section>
            <div class="q-pa-md">
              <div class="q-gutter-md" style="max-width: 300px">
                  <q-input outlined color="white" label="NAME">
                    <template v-slot:prepend>
                      <q-icon name="event" />
                    </template>
                  </q-input>
                </div>
              </div>
              <div class="q-pa-md">
              <div class="q-gutter-md" style="max-width: 300px">
                  <q-input outlined color="white" label="PASSWORT">
                    <template v-slot:prepend>
                      <q-icon name="event" />
                    </template>
                  </q-input>
                </div>
              </div>
        </q-card-section>

        <q-card-actions align="right" class="bg-white text-teal">
          <q-btn flat label="SHOW ME" @click="dialog = false"/>
        </q-card-actions>
      </q-card>
    </q-dialog>
          <!-- ENDE HEADER -->
    </q-toolbar>
    </q-header>

    <q-page-container class="aaa">
      <router-view />
    </q-page-container>

    <q-footer elevated class="text-black">
      <q-toolbar>
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
      scrollPos: false,
      dialog: false,
      isTop: true,
      scrollInfo: { }
    }
  },
  methods: {
    openURL,
    instagram (thisURL) {
      openURL(thisURL)
    },
    github (thisURL) {
      openURL(thisURL)
    },
    onScroll (info) {
      this.scrollInfo = info
      if (info.position === 0) {
        this.isTop = true
      } else {
        this.isTop = false
      }
    }
  }
}
</script>

<style>

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

.aaa {
  padding-top: 0px !important
}

.toptop {
  background-color: #FFFFFF00;
  transition: all 0.5s ease;
  color: white
}

.nottop {
  color: black
}
</style>

<template>
  <div class="q-pt-none">
    <q-parallax :height="750" :speed="3.0">
      <template v-slot:media>
        <img src="statics/IMG_20190217_190350.jpg">
      </template>
      <h1 class="text-white">JASON</h1>
    </q-parallax>

    <br><br><br><br><br>

    <div>
      <q-knob
      :min="20"
      :max="70"
      v-model="value22"
      show-value
      size="50px"
      :thickness="0.22"
      color="teal"
      track-color="grey-3"
      class="q-ma-md"
    />
    FÄHIGKEITEN!
    </div>
    <br>
    <div>
      <q-circular-progress
      reverse
      :value="value"
      size="40px"
      :thickness="0.4"
      color="light-blue"
      track-color="grey-3"
      center-color="grey-9"
      class="q-ma-md"
    />
    Skills
    </div>
    <div class="q-gutter-md row mitte">
      <div>adsasd</div><br>
      <q-linear-progress style="height: 10px" :value="progress" color="black" class="col-3"></q-linear-progress>
    </div>
    <br><br><br>
</div>
</template>

<style>
.mitte {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>

<script>
export default {
  name: 'PageIndex',
  data () {
    return {
      value: 71,
      value22: 55,
      progress: 0.4
    }
  }
}
</script>

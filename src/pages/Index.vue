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

      <q-linear-progress style="height: 10px" :value="progress" color="black" class="col-3"></q-linear-progress>

      <div color="black" class="col-3">sadasd</div>

 

      <q-linear-progress rounded style="height: 20px" :value="progress" color="warning" class="q-mt-sm" ></q-linear-progress>

 

      <q-linear-progress rounded style="height: 15px" :value="progress" color="secondary" class="q-mt-sm" ></q-linear-progress>

 

      <q-linear-progress style="height: 25px" :value="progress" color="accent" class="q-mt-sm" ></q-linear-progress>
    </div>
 

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
      progress: 0.4
    }
  }
}

</script>
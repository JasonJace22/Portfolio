<template>
  <q-page class="flex flex-center">
    <p>Scroll Up and Down this page to see the parallax scrolling effect.</p>
    <div class="parallax"></div>
    <div style="height:1000px;background-color:red;font-size:20px">
        Scroll Up and Down this page to see the parallax scrolling effect.
        This div is just here to enable scrolling.
        Tip: Try to remove the background-attachment property to remove the scrolling effect.
        </div>
  </q-page>
</template>

<style>
.parallax {
/* The image used */
background-image: url("/statics/IMG_20190217_190350");
/* Set a specific height */
min-height: 800px;
/* Create the parallax scrolling effect */
background-attachment: fixed;
background-position: center;
background-repeat: no-repeat;
background-size: cover;
}
</style>

<script>
export default {
  name: 'PageIndex'
}
</script>

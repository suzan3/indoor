<template>
  <q-page class="flex flex-center">
   <cover></cover>
   <monitor></monitor>
   <mobileApp></mobileApp>
  </q-page>
</template>

<script>
import cover from 'pages/cover.vue';
import monitor from 'pages/monitor.vue';
import mobileApp from 'pages/mobileApp.vue';
import '../css/fonts.scss';

export default {
  name: 'PageIndex',
  components:{
    cover,
    monitor,
    mobileApp
  }
}
</script>

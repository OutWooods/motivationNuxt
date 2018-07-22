<template>
  <div>
    <button @click="newPixl">Click me</button>
    <div id="pixl-box"></div>
  </div>
</template>

<script>

  import Pixl from '~/components/Pixl.vue'
  import Vue from 'vue'

  export default {
    components: {
      Pixl
    },

    methods: {
      newPixl: () => {
        const PixlConstructor = Vue.extend(Pixl);
        var newPixl = new PixlConstructor();
        newPixl.$mount();

        document.getElementById('pixl-box').appendChild(newPixl.$el);
      }
    }
  }


</script>


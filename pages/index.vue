<template>
  <div>
      <div id="box"></div>
      <button @click="newPixl">Click me</button>
  </div>
</template>

<style>
</style>

<script>

  import Pixl from '~/components/Pixl.vue'
  import Vue from 'vue'

  export default {
    components: {
      Pixl
    },

    mounted() {
      console.log(this.$refs.box);
    },

    methods: {
      newPixl: () => {
        const PixlConstructor = Vue.extend(Pixl);
        var newPixl = new PixlConstructor();
        newPixl.$mount();

        document.getElementById('box').appendChild(newPixl.$el);
      }
    }
  }


</script>


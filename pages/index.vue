<template>
  <div>
    <h1 class="text-center pb-6"> The Great Motivational Pixl's Site</h1>
    <div class="container">
      <div id="pixl-box"></div>
      <div class="targets">
        <p class="pl-6 pr-6">Spent 30mins doing coding</p>
        <button @click="newPixl"
                class="bg-blue hover:bg-blue-dark text-white font-bold py-2 px-4 rounded">
          Target Achieved
        </button>
      </div>
    </div>
  </div>
</template>

<style>
  .container {
    display: flex;
    justify-content: space-around;
  }

  #pixl-box {
    display: flex;
    flex-wrap: wrap;
    width: 50%;
  }

  .targets {
    display: flex;
  }

</style>

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


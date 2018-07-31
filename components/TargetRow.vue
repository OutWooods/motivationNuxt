<template>
  <li :style="{ backgroundColor: colour }">
    <button @click="newPixl"
            class="bg-blue hover:bg-blue-dark text-white font-bold py-2 px-4 rounded">
      Target Achieved
    </button>
    <span> {{ name }} </span>
  </li>
</template>

<script>
  import Pixl from '~/components/Pixl.vue'
  import Vue from 'vue'

  export default {
    components: {
      Pixl,
    },

    props: [
      'name',
      'store',
      'colour',
    ],

    methods: {
      newPixl: function() {
        const PixlConstructor = Vue.extend(Pixl);
        let newPixl = new PixlConstructor({
          propsData: {
            colour: this.colour,
          }
        });
        newPixl.$mount();
        document.getElementById(this.store).appendChild(newPixl.$el);
      },
    }
  }
</script>


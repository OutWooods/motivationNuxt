<template>
  <div>
    <h1 class="text-center pb-6"> The Great Motivational Pixl's Site</h1>
    <div class="container">
      <div :id="store"></div>
      <ul id="targets">
        <li>
          <input v-model="message" placeholder="Target Name">
          <input v-model="colourChoice.red" placeholder="colourChoice.red">
          <input v-model="colourChoice.blue" placeholder="colourChoice.blue">
          <input v-model="colourChoice.green" placeholder="colourChoice.green">
          <button @click="randomColour"
                  class="bg-orange hover:bg-orange-dark text-white font-bold py-2 px-4 rounded">
            Random colour
          </button>
          <button @click="newTarget"
                  class="bg-green hover:bg-green-dark text-white font-bold py-2 px-4 rounded">
            Add new target
          </button>
        </li>
      </ul>
    </div>
  </div>
</template>

<style>
  ul {
    list-style-type: none;
  }

  .container {
    display: flex;
    justify-content: space-around;
  }

  #pixl-box {
    display: flex;
    flex-wrap: wrap;
    width: 50%;
  }
</style>

<script>

  import TargetRow from '~/components/TargetRow.vue'
  import Vue from 'vue'

  export default {
    components: {
      TargetRow,
    },

    data() {
      return {
        'message': '',
        'store': 'pixl-box',
        'colourChoice': {
          'red': 0,
          'blue': 0,
          'green': 0,
        }
      };
    },

    methods: {
      colourMaker: function () {
        return `rgb(${this.colourChoice.red}, ${this.colourChoice.blue}, ${this.colourChoice.green})`
      },

      randomColour: function () {
        this.colourChoice.blue = Math.round(Math.random() * 255);
        this.colourChoice.red = Math.round(Math.random() * 255);
        this.colourChoice.green = Math.round(Math.random() * 255);
      },

      reset: function () {
        this.colourChoice.red = 255;
        this.colourChoice.blue = 255;
        this.colourChoice.green = 255;
        this.message = '';
      },

      newTarget: function () {
        const TargetRowConstructor = Vue.extend(TargetRow);
        let newTargetRow = new TargetRowConstructor({
          propsData: {
            'name': this.message,
            'store': this.store,
            'colour': this.colourMaker(),
          }
        });
        newTargetRow.$mount();
        const targets = document.getElementById('targets');
        const secondLastNode = targets.childNodes.length - 1;

        targets.insertBefore(newTargetRow.$el, targets.childNodes[secondLastNode]);
        this.reset();
      }
    }
  }


</script>


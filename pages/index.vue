<template>
  <div>
    <h1 class="text-center pb-6"> The Great Motivational Pixl's Site</h1>
    <div class="container">
      <div id="pixl-box"></div>
      <li id="targets">
        <ul>
          <p class="pl-6 pr-6">Spent 30mins doing coding</p>
          <button @click="newPixl"
                  class="bg-blue hover:bg-blue-dark text-white font-bold py-2 px-4 rounded">
            Target Achieved
          </button>
        </ul>
        <ul>
          <p class="pl-6 pr-6"> Add new target</p>
          <button @click="newTarget"
                  class="bg-green hover:bg-green-dark text-white font-bold py-2 px-4 rounded">
            Add New Target
          </button>
        </ul>
      </li>
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
      },

      newTarget: () => {
        console.log(document.getElementById('pixl-box'));
       console.log(document.getElementById('targets'));
       const div = document.createElement('ul');
       div.innerHTML = 'target2';
       const targets = document.getElementById('targets');
       const secondLastNode = targets.childNodes.length -1;
       targets.insertBefore(div, targets.childNodes[secondLastNode]);
      }
    }
  }


</script>


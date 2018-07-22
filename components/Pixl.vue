<template>
  <div class="pixl h-3 w-3" v-bind:style="{ backgroundColor: colourMaker() }">
  </div>
</template>

<style>
</style>


<script>
  export default {
    created: function () {
      this.colourMaker();
    },

    methods: {
      colourMaker: () => {
        return `rgb(${Math.random() * 255}, ${Math.random() * 255}, ${Math.random() * 255})`
      }
    }
  }
</script>

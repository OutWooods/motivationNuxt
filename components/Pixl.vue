<template>
  <div class="pixl" v-bind:style="{ backgroundColor: colourMaker() }">
  </div>
</template>

<style>
  .pixl {
    height: 10px;
    width: 10px;
  }
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

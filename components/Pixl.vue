<template>
  <div class="pixl h-4 w-4" :style="{ backgroundColor: colour }">
  </div>
</template>

<script>
  export default {
    props: [
      'colour',
    ],
  }
</script>

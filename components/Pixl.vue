<template>
  <div class="pixl h-3 w-3" :style="{ backgroundColor: colour }">
  </div>
</template>

<script>
  export default {
    props: [
      'colour',
    ],
  }
</script>

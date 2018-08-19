<template>
  <div class="flex">
    <div class="flex-1 flex flex-wrap">
      <pixl :colour="pixl.colour"
            :key="pixl.id"
            v-for="pixl in pixls"
      >
      </pixl>
    </div>
    <div class="ml-auto flex-col">
      <div>
        <button @click="addTarget">
          New Target
        </button>
      </div>
      <div :key="target.id"
           v-for="target in targets">
        <button @click="addPixl(target.colour)"
                class="bg-blue hover:bg-blue-dark text-white font-bold py-2 px-4 rounded"
        >Add goal
        </button>
      </div>
    </div>
  </div>
</template>

<script>
  import Pixl from '~/components/Pixl.vue'

  export default {
    components: {
      Pixl,
    },

    data() {
      return {
        targets: [{
          'id': 1,
          'colour': 'purple',
        }],
        pixls: [{
          'id': 1,
          'colour': 'blue',
        },],
      };
    },

    methods: {
      addPixl(colour) {
        this.pixls.push({
          id: `pixl-${this.pixls.length}`,
          colour: colour,
        });
      },
      addTarget() {
        this.targets.push({
          id: `target-${this.targets.length}`,
          colour: 'yellow',
        });
      },
    },
  };
</script>

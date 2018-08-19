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
        <input v-model="newTarget.name">
        <input v-model="newTarget.colour">
        <button @click="addTarget">
          New Target
        </button>
      </div>
      <div :key="target.id"
           v-for="target in targets">
        <span v-text="target.name"></span>
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
        newTarget: {
          name: '',
          colour: '',
        },
        targets: [],
        pixls: [],
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
        this.newTarget.id = this.targets.length;
        this.targets.push(JSON.parse(JSON.stringify(this.newTarget)));
        this.newTarget.name = '';
        this.newTarget.colour = '';
      },
    },
  };
</script>

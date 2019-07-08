<template>
  <div style="height: 200vh">
    <button v-on:click="toggle">Toggle</button>
    <Treeselect v-if="showTreeselect" v-bind:options="[]" v-bind:always-open="true" />
  </div>
</template>

<script>
import Treeselect from '@riophae/vue-treeselect';
export default {
  components: { Treeselect },
  methods: {
    toggle: function() {
      this.showTreeselect = !this.showTreeselect;
    },
  },
  data: function() {
    return {
      showTreeselect: false,
    };
  },
};
</script>

<style>
@import '~@riophae/vue-treeselect/dist/vue-treeselect.css';
</style>

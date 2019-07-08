<template>
  <Treeselect v-bind:options="[]" v-bind:always-open="true" />
</template>

<script>
import Treeselect from '@riophae/vue-treeselect';
export default {
  components: { Treeselect },
};
</script>

<style>
@import '~@riophae/vue-treeselect/dist/vue-treeselect.css';
</style>

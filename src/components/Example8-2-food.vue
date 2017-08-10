<template>
  <button class="btn btn-success btn-lg" @click="voted">Vote</button>
</template>

<script>
export default {
  name: 'Example8-2',
  data() {

  },
  methods: {
    voted() {
      this.$emit('voted');
    },
  },
};
</script>

<style>

</style>

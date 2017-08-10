<template>
  <button class="btn btn-info btn-lg" @click="voted">Sushi 🍣</button>
</template>

<script>
export default {
  name: 'Example8-2',
  methods: {
    voted() {
      this.$emit('voted');
    },
  },
};
</script>

<style>

</style>

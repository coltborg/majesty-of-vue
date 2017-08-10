<template>
  <div class="container">
    <h1>Example 8.1</h1>
    <div class="text-center">
      <p style="font-size: 15rem;">
        {{ votes }}
      </p>
      <button class="btn btn-success btn-lg" @click="vote">Vote</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Example8-1',
  data() {
    return {
      votes: 0,
    };
  },
  methods: {
    vote() {
      this.$emit('voted');
    },
  },
  created() {
    this.$on('voted', () => {
      /* eslint-disable no-plusplus */
      this.votes++;
    });
  },
};
</script>

<style>

</style>

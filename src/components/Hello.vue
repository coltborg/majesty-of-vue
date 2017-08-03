<template>
  <div class="hello">
    <button type="button" @click="upvote">Upvote! ({{ upvotes }})</button>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data() {
    return {
      upvotes: 0,
    };
  },
  methods: {
    upvote() {
      this.upvotes += 1;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>

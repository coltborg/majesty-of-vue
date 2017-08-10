<template>
  <div class="container">
    <h1>Example 8.2</h1>
    <div class="text-center">
      <p style="font-size: 15rem;">
        {{ votes }}
      </p>
      <example82-food @voted="countVote"></example82-food>
    </div>
  </div>
</template>

<script>
import Example82Food from './Example8-2-food';

export default {
  name: 'Example8-2',
  components: {
    Example82Food,
  },
  data() {
    return {
      votes: 0,
    };
  },
  methods: {
    countVote() {
      this.votes += 1;
    },
  },
};
</script>

<style>

</style>

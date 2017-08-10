<template>
  <div class="container">
    <h1>Example 8.3</h1>
    <div class="text-center">
      <p style="font-size: 15rem;">
        {{ votes }}
      </p>
      <div class="row">
        <example83-food @voted="countVote" name="Sushi 🍣" color="btn-info"></example83-food>
        <example83-food @voted="countVote" name="Pizza 🍕" color="btn-warning"></example83-food>
        <example83-food @voted="countVote" name="Ramen 🍜" color="btn-default"></example83-food>
      </div>
      <h2>Log:</h2>
      <ul class="list-group">
        <li class="list-group-item" v-for="(vote, index) in log" :key="index">
          {{ vote }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import Example83Food from './Example8-3-food';

export default {
  name: 'Example8-3',
  components: {
    Example83Food,
  },
  data() {
    return {
      votes: 0,
      log: [],
    };
  },
  methods: {
    countVote(food) {
      this.votes += 1;
      this.log.push(`${food} received a vote.`);
    },
  },
};
</script>

<style>

</style>

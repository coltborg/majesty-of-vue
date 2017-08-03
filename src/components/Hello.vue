<template>
  <div class="hello">
    <h1>People of Vue</h1>
    <ul>
      <li v-for="person in people" :key="person.name">{{ person.name }} ({{ person.votes }}) <button type="button" @click="person.votes++">Vote</button></li>
    </ul>
    <input type="text" placeholder="Enter delete to reset">
    <h1>Our Mayor is {{ winner.name }}</h1>

    <pre>{{ $data }}</pre>
    <pre>{{ winner }}</pre>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data() {
    return {
      people: [{
        name: 'Kevin',
        votes: 0,
      }, {
        name: 'Mike',
        votes: 0,
      }, {
        name: 'Lisa',
        votes: 0,
      }, {
        name: 'Colt',
        votes: 0,
      }],
    };
  },
  computed: {
    winner() {
      const compareVotes = this.people.sort((a, b) => b.votes - a.votes);
      return compareVotes[0];
    },
  },
  methods: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
pre {
  background-color: #e0e0e0;
  padding: 0.5rem;
}
</style>

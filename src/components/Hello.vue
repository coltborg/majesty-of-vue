<template>
  <div class="hello">
    <h1>Real super hero identities</h1>
    <ul>
      <li v-for="hero in heros" :key="hero">
        {{ hero | snitch }}
      </li>
    </ul>

    <pre>{{ $data }}</pre>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data() {
    return {
      heros: [
        {
          firstName: 'Bruce',
          lastName: 'Wayne',
          secretId: 'Batman',
        }, {
          firstName: 'Clark',
          lastName: 'Kent',
          secretId: 'Superman',
        },
      ],
    };
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

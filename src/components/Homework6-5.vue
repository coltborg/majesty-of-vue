<template>
  <div class="container">
    <h1>Homework 6.5</h1>
    <ul class="list-group">
      <li v-for="person in orderedPeople()" class="list-group-item" :key="person.name">
        {{ person.name }} {{ person.age }}
      </li>
    </ul>
    <ul class="list-group">
      <li v-for="person in old" class="list-group-item" :key="person.name">
        {{ person.name }} {{ person.age }}
      </li>
    </ul>
  </div>
</template>

<script>
import _ from 'lodash';

export default {
  name: 'Homework6-5',
  data() {
    return {
      people: [
        {
          name: 'Obelix',
          age: 33,
        },
        {
          name: 'Asterix',
          age: 32,
        },
        {
          name: 'Majestix',
          age: 82,
        },
        {
          name: 'Methusalix',
          age: 103,
        },
        {
          name: 'Julius Caesar',
          age: 66,
        },
      ],
    };
  },
  methods: {
    orderedPeople() {
      return _.orderBy(this.people, 'age');
    },
  },
  computed: {
    old() {
      return this.people.filter(item => item.age > 65);
    },
  },
};
</script>

<style>

</style>

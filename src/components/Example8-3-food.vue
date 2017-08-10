<template>
  <div class="col-lg-4 text-center">
    <p style="font-size: 10rem;">
      {{ votes }}
    </p>
    <button class="btn btn-lg" :class="color" @click="voted">
      {{ name }}
    </button>
  </div>
</template>

<script>
export default {
  name: 'Example8-3-food',
  props: [
    'name',
    'color',
  ],
  data() {
    return {
      votes: 0,
    };
  },
  methods: {
    voted(event) {
      this.votes += 1;
      this.$emit('voted', event.srcElement.textContent);
    },
  },
};
</script>

<style>

</style>

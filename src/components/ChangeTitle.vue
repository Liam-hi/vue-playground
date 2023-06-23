<template>
    <div>
      <div>
        <h1>{{ title }}</h1>
        <p>{{ text }}</p>
      </div>
      <button v-on:click="changeTitle">Submit</button>
    </div>
  </template>
  

<script>
export default {
  data() {
    return {
      title: "Hello Vue!"
    };
  },
  methods: {
    changeTitle() {
      this.title = "Hello World!"
    }
  },
  props: {
    text: {
      type: String,
      default: "Default text"
    }
  }
}
</script>

<style scoped>
p {
    color: red;
}
</style>


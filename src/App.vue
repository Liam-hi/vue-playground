<template>
  <h1>My First Vue app</h1>
  <ChangeTitle :text="'Welcome to my first webpage!'"/>
  <button @click="handleToggle">Toggle</button>
  <CardItem v-if="toggle" :text="'First Card'"/>
  <CardItem v-else :text="'Second Card'"/>
  <ConditionalRendering />
</template>

<script>
import ChangeTitle from './components/ChangeTitle.vue'
import CardItem from './components/CardItem.vue'
import ConditionalRendering from './components/ConditionalRendering.vue'

export default {
  name: 'App',
  components: {
    ChangeTitle,
    CardItem,
    ConditionalRendering
  },
  data() {
    return {
      componentTitle: "Component Title",
      toggle: true,
    }
  },
  methods: {
    handleToggle() {
      this.toggle = !this.toggle
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

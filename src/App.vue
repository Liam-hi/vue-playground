<template>
  <h1>My First Vue app</h1>
  <ChangeTitle :text="'Welcome to my first webpage!'"/>
  <button @click="handleToggle">Toggle</button>
  <CardItem v-if="toggle" :text="'First Card'"/>
  <CardItem v-else :text="'Second Card'"/>
  <ConditionalRendering />
  <CounterApp />
  <IncrementArray />
  <UsingRefs />
  <ArrayProps :items="myArray" />
  <AnimateHeader />
  <ScrollTriggerAnimation />
  <AnimateToggle />
  <ScriptSetup />
  <ScriptSetupGSAP />
</template>

<script>
import ChangeTitle from './components/ChangeTitle.vue'
import CardItem from './components/CardItem.vue'
import ConditionalRendering from './components/ConditionalRendering.vue'
import CounterApp from './components/CounterApp.vue'
import IncrementArray from './components/IncrementArray.vue'
import UsingRefs from './components/UsingRefs.vue'
import ArrayProps from './components/ArrayProps.vue'
import AnimateHeader from './components/AnimateHeader.vue'
import ScrollTriggerAnimation from './components/ScrollTriggerAnimation.vue'
import AnimateToggle from './components/AnimateToggle.vue'
import ScriptSetup from './components/ScriptSetup.vue'
import ScriptSetupGSAP from './components/ScriptSetupGSAP.vue' 

export default {
  name: 'App',
  components: {
    ChangeTitle,
    CardItem,
    ConditionalRendering,
    CounterApp,
    IncrementArray,
    UsingRefs,
    ArrayProps,
    AnimateHeader,
    ScrollTriggerAnimation,
    AnimateToggle,
    ScriptSetup,
    ScriptSetupGSAP
  },
  data() {
    return {
      componentTitle: "Component Title",
      toggle: true,
      myArray: [
        { id: 1, name: 'Item 1' },
        { id: 2, name: 'Item 2' },
        { id: 3, name: 'Item 3' },
      ],
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

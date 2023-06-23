<template>
    
    <button @click="handleActive(0)">First</button>
    <button @click="handleActive(1)">Second</button>
    <button @click="handleActive(2)">Third</button>
    <CardItem :text="'First Card'" v-if="active === 0"/>
    <CardItem :text="'Second Card'" v-else-if="active === 1"/>
    <CardItem :text="'Third Card'" v-else-if="active === 2"/>
</template>

<script>
import CardItem from './CardItem.vue'

export default {
    components: {
        CardItem
    },
    data() {
        return {
            active: 0
        }
    },
    methods: {
        handleActive(num) {
            this.active = num;
        }
    }
  }
  </script>

<style scoped>

div {
    display: flex;
    align-items: center;
    justify-content: center;
    background: pink;
    height: 128px;
    width: 128px;
}
</style>
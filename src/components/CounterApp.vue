<template>
    <h1>{{ counter }}</h1>
    <button @click="handleIncrease">Increase</button>
    <button @click="handleDecrease">Decrease</button>
    <button @click="handleReset">Reset</button>
</template>

<script>
export default {
    data() {
        return {
            counter: 0
        }
    },
    methods: {
        handleIncrease() {
            this.counter++;
        },
        handleDecrease() {
            this.counter--;
        },
        handleReset() {
            this.counter = 0;
        },
    }
}
</script>
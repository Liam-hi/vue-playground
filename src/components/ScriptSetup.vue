<template>
    <p>{{ count }}</p>
    <button @click="increment">Increment</button>
    <button @click="decrease">Decrease</button>
    <button @click="reset">Reset</button>
</template>

<!-- Om du vill slippa skriva app(), method, unmounted och så vidare -->

<script setup>
import { ref, onUnmounted } from 'vue';

const count = ref(0);

function increment() {
    count.value++;
}

function decrease() {
    count.value--;
}

function reset() {
    count.value = 0;
}

onUnmounted(() => {
    // Your cleanup logic here
    console.log('Component unmounted');
});

</script>
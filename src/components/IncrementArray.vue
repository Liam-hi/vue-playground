<template>
    <br>
    <button @click="handleIncrement">Increment</button>
    <br>
    {{ title }}

</template>

<script>
export default {
    data() {
        return {
            currentIndex: 1,
            arr: ['första', 'andra', 'tredje'],
            title: 'första'
        }
    },
    methods: {
        handleIncrement() {
            this.title = this.arr[this.currentIndex];
            this.currentIndex++;
            if (this.currentIndex === this.arr.length) {
                this.currentIndex = 0;
            }
        }
    }
}
</script>
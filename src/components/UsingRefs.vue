<template>
    <div class="wrapper">
        <button @click="addClass">Change class.</button>
        <div class="box" ref="changeClass"></div>
    </div>

</template>

<script>
export default {
    methods: {
        addClass() {
            this.$refs.changeClass.classList.add('blue')
        }
    }
}
</script>

<style>
.wrapper {
    display: flex;
    flex-direction: column;
    align-items: center
}

.box {
    height: 48px;
    width: 48px;
    background: red;
}

.blue {
    background: blue;
}
</style>
<template>
    <div class="container">
        <button ref="button">Animate</button>
        <br>
        <div class="square" ref="box">

        </div>
    </div>
</template>

<script setup>
import { onMounted, ref } from "vue";
import { gsap } from "gsap";

const box = ref();
const button = ref();
const tl = gsap.timeline();

onMounted(() => {
    tl.to(box.value, {
        rotate: 20,
        x:50,
        color: "red",
        duration: 2
    });
        
    tl.reverse();
    
    function menu() {
        tl.reversed(!tl.reversed());
    }

    button.value.addEventListener("click", menu);
});

</script>


<style>
.container {
    height: 100%;
    width: 100%;
    display: flex;
    justify-content: center;
}
.square {
    height: 48px;
    width: 48px;
    background: lightcoral;
}
</style>
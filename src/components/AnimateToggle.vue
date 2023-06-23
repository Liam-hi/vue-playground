<template>
     <button ref="clickEvent">Animate</button>
    <h1 ref="animateHeader">
        Animate header
    </h1>

</template>

<script>
import { gsap } from 'gsap';

export default {
    methods: {
        handleAnimate() {

        }
    },
    mounted() {
        const element = this.$refs.animateHeader;
        const tl = gsap.timeline();
        
        tl.to(element, {
            rotate: 20,
            color: "red",
            duration: 2
        });
        

        tl.reverse();

        function menu() {
            tl.reversed(!tl.reversed());
        }

        this.$refs.clickEvent.addEventListener("click", menu);

        


 
    }
}
</script>
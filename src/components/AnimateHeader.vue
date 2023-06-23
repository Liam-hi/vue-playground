<template>
    <h1 ref="animateHeader">
        Animate header
    </h1>

</template>

<script>
import { gsap } from 'gsap';

export default {
    methods: {
        handleAnimate() {
            const element = this.$refs.animateHeader;

            gsap.to(element, {
                rotate: 20,
                color: "red",
                duration: 2
            })
        }
    },
    mounted() {
        this.handleAnimate();
    }
}
</script>
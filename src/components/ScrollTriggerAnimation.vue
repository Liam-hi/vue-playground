<template>
    <h1 ref="element">
        Animate header
    </h1>

</template>

<script>
    import { gsap } from 'gsap';
    import { ScrollTrigger } from 'gsap/ScrollTrigger';

    gsap.registerPlugin(ScrollTrigger);

export default {
    methods: {
        handleAnimate() {
            const element = this.$refs.element;

            gsap.to(element, {
                rotate: 20,
                color: "red",
                duration: 2,
                scrollTrigger: {
                    trigger: element,
                    start: 'top 80%',
                    end: 'bottom 20%',
                }
            })
        }
    },
    mounted() {
        this.handleAnimate();
    }
}
</script>

<style scoped>

h1 {
    padding-top: 400px;
}

</style>



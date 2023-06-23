<template>
    <div>
        <ul>
            <li v-for="x in items" :key="x.id">
                {{ x.name }}
            </li>
        </ul>
    </div>

</template>

<script>
export default {
    props: {
        items: {
            type: Array,
            required: true,
        }
    }
}
</script>
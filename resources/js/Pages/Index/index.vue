<template>Hello ! {{ counter }}</template>


<script>
import { ref, onMounted } from 'vue';

export default {
    setup() {
        const counter = ref(0)

        onMounted(() => {
            setInterval(() => counter.value++, 1000)
        })

        return { counter }
    }
}
</script>

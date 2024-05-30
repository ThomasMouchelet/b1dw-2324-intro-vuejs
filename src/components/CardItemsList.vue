<script setup>
    import { defineProps } from 'vue'

    const props = defineProps({
        title: String
    })
</script>

<template>
    <h2>{{ props.title }}</h2>

    <!-- List all items into cardList -->
</template>
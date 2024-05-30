<script setup>
    import { defineProps, ref, watch } from 'vue'

    const totalPrice = ref(0)

    const props = defineProps({
        title: String,
        cardItemsList: Array
    })

    console.log("props:", props.cardItemsList)

    // Watcher for cardItemsList
    watch(props.cardItemsList , (newVal, oldVal) => {
        console.log("props.cardItemsList watch:", props.cardItemsList)
        totalPrice.value = newVal.reduce((acc, item) => acc + item.price, 0)
    })
</script>

<template>
    <h2>{{ props.title }}</h2>

    <!-- List all items into cardList -->
    <ul>
        <li v-for="item in props.cardItemsList">
            <h3>{{ item.title }}</h3>
            <p>{{ item.price }}</p>
            <button @click="$emit('removeItemCard', item)">
                Remove
            </button>
        </li>
    </ul>

    <p>
        Total price: {{ totalPrice }}
    </p>
</template>
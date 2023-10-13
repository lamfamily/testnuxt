<script setup lang="ts">
const counter = ref(0);

const counterDouble = computed(() => counter.value * 2);

const increment = () => counter.value++;
const decrement = () => counter.value--;

</script>

<template>
    <div
        class="fixed top-1/2 left-1/2 transform translate-x-[-50%] translate-y-[-50%]"
    >
        <h1 class="text-3xl">Counter: {{ counter }}</h1>
        <h1 class="text-3xl">Counter double: {{ counterDouble }}</h1>

        <button
            class="bg-blue-500 rounded px-2 py-1 text-white hover:bg-blue-700"
            @click="increment"
        >
            Increment
        </button>
        <button
            class="bg-gray-500 rounded px-2 py-1 text-white hover:bg-gray-700"
            @click="decrement"
        >
            Decrement
        </button>
    </div>
</template>

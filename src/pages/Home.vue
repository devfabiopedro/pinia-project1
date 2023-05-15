<template>
    <div>
        <h2>Página inicial</h2>
        <hr>
        Contagem atual: {{ counter.count }}
        <button @click="counter.increment">+</button>
        <button @click="counter.decrement">-</button>
    </div>
</template>

<script setup>
import { useCounterStore } from '../stores/CounterStore'

const counter = useCounterStore()

counter.count++
counter.$patch({count: counter.count + 1})
counter.increment()

</script>

<style scoped>

</style>
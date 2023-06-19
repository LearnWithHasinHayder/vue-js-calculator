<script setup>
import { ref } from 'vue'

const x = ref(0)
const y = ref(0)
const result = ref(0)
</script>
<template>
    <div class="card">
        <input id="x" class="number" type="text" v-model="x">
        <button id="add" @click="result = parseInt(x) + parseInt(y)" type="button"> + </button>
        <button id="sub" @click="result = x - y" type="button"> - </button>
        <button id="mul" @click="result = x * y" type="button"> x </button>
        <button id="div" @click="result = x / y" type="button"> / </button>
        <input id="y" class="number" type="text" v-model="y">
        =
        <input id="result" class="number" type="text" v-model="result">
    </div>
</template>
<style>
.number {
    padding: 0.6em 1.2em;
    width: 50px;
}
</style>
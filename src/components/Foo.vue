<script setup>
import { PageData } from "/src/data/data.js"
const node_key = import.meta.env.VITE_NODE_KEY;
</script>

<template>

    <div class="container">
        <div v-for="d in PageData" :key="d">
            {{d.image}}
        </div>
    </div>
</template>

<style scoped>
* {
    color: white;
}

.container {
    display: grid;
    grid-template-columns: auto;
    justify-content: center;
    align-items: center;
    width: 100vh;
    height: 80vh;
}
</style>

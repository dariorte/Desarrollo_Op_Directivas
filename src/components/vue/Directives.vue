<script setup>
import { ref } from 'vue'
// Codigo de manera repetitiva
const users = ["Pepe ","Ana ","Juana ","Lola "]

const isCheckd= ref(true)
</script>
<template>
    <ul>
        <!-- Estamos extrayendo los usuarios que estan dentro del array [users] -->
        <li v-for="(user, i) in users" :key="i"> {{i}} {{ user }}</li>
    </ul>

    <!-- Cuando utilizemos elementos de formulario utilizemos un label -->
    <input type="checkbox" id="check" v-model="isCheckd">
    <label for="check">Pinchame</label>
    <div class="bg-blue-400 text-white rounded py-1 px-2"
    :class="{'bg-orange-500': isCheckd}">
        Este es un mensaje
    </div>
    <!-- lo que esta entre las comillas se toma como codigo javascritp -->
    <div v-show="isCheckd">
        Este es un mensaje que podria ocultar
    </div>
    <div v-if="isCheckd">
        Este es un mensaje que podrìa ocultar
    </div>
    <div v-else>
        Esto se ve porque no cumpliò la condiciòn del if
    </div>

    <!-- ///////////////////////////////////////////////////////////////////////////// -->
</template>
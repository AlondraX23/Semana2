<script setup>
import { ref } from 'vue';
import { RouterLink } from 'vue-router';

const item = ref();
console.log(item)
let listaPokemon = ref([]);
const urlPokemon = ref([]);

function obtUrl() {
    // const value = item.url 
    urlPokemon.value.push(item.url)
    // console.log(value)
}

fetch('https://pokeapi.co/api/v2/pokemon')
    .then(res => res.json())
    .then((data) => {
        listaPokemon.value = data.results;
    })


</script>

<template>
    <div class="container py-4 main">
        <ul class="list-group" v-for="item in listaPokemon">
            <li class="list-group-item border border-0">
                <RouterLink :to="`/contenido/${item.name}`" class="link-underline link-underline-opacity-0" @click="obtUrl">
                    {{ item.name }}
                </RouterLink>
            </li>
            <span style="visibility: collapse ;">{{ item.url }}</span>
            <hr>
        </ul>
    </div>
</template>

<style>
hr {
    color: red;
    border-width: 2px;
}
</style>

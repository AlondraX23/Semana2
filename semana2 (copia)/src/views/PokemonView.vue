<script setup>
import { ref } from 'vue';
import { useRouter } from 'vue-router';
// import Card from './components/Card.vue';




// var namePokemon = this.$route.params.name;
// alert(namePokemon)

// mounted() {
//     const id = this.$route.params.id;
//     console.log(id);
// }

// const infoPokemon = ref([])
// onMounted( async () => {
//     const id = this.$route.params.id;
//     console.log(id);
//     const data = await fetch(`https://pokeapi.co/api/v2/${route.params.name}/`);
//     const res = data.json();
//     console.log(res)
//     infoPokemon.value =res;
//     // console.log(infoPokemon.value)
// })



// var pokemonName = this.$route.params.name
// console.log(pokemonName)

// var endPoint = `https://pokeapi.co/api/v2/${route.params.name}/`;
// console.log(endPoint)
//     // Llamado a la API graphic_1
//     fetch(endPoint)

//         // Promesa cuando se cumple o cuando la respuesta es exitosa
//         .then(function (respuesta) {
//             return respuesta.json();
//         })

//         // Promesa recibe los datos en formato JSON
//         .then(function (datos) {
//             var peso = datos.weight;
//             var altura = datos.height;
//             var nombre = datos.name;
//             var experiencia = datos.base_experience;

//             peso = (peso / 10).toFixed(1);
//             altura = (altura / 10).toFixed(1);
//             nombre = nombre.charAt(0).toUpperCase() + nombre.slice(1);

//             var img = datos.sprites.front_default;

//         })
// console.log(endPoint)

// var endPoint = `https://pokeapi.co/api/v2/pokemon/${pokemon.name}`

// fetch(`https://pokeapi.co/api/v2/pokemon/${route.params.name}`)
//     .then(res => res.json())
//     .then((data) => {
//         listaPokemon.value = data.results;
//     })

// var infoPokemon = ref([])

// fetch(`https://pokeapi.co/api/v2/${route.params.name}/`)
//     .then((res) => res.json())
//     .then((data) => {infoPokemon.value = data, console.log})

const router = useRouter()
const volver = () => {
    router.push('/contenido')
};
</script>

<template>
    <section class="container py-4 main">
        <h1>{{ $route.params.name }}</h1>
        <!-- <template v-for="item in infoPokemon"></template> -->
        <div class="card mb-3" style="max-width: 540px;">
            <div class="row g-0">
                <div class="col-md-4">
                    <img :src="img" class="img-fluid rounded-start" alt="...">
                    <!-- <img :src="item.sprites.front_default" class="img-fluid rounded-start" alt="..."> -->
                </div>
                <div class="col-md-8">
                    <div class="card-body">
                        <h5 class="card-title">{{ $route.params.name }}</h5>
                        <p class="card-text">This is a wider card with supporting text below as a natural lead-in to
                            additional
                            content. This content is a little bit longer.</p>
                        <p class="card-text"><small class="text-body-secondary">Last updated 3 mins ago</small></p>
                    </div>
                </div>
            </div>
        </div>
        <button type="button" class="btn btn-outline-danger mt-2" @click="volver"> Volver</button>

    </section>
</template>
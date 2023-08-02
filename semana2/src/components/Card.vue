<!-- <script setup>
defineProps({
    titulo: String,
    texto: String,
    imagen: String,
    color_card: String,
    color_text:{
        type: String,
        default: 'text-dark'
    }
})

const router = useRouter()
const volver = () => {
    router.push('/contenido')
};
</script>

<template>
    <div class="col">
        <div class="card" :class="color_card">
            <img :src="imagen" class="card-img-top" :alt="titulo">
            <div class="card-body" :class="color_text">
                <h5 class="card-title">{{ titulo }}</h5>
                <p class="card-text">{{ texto }}</p>
            </div>
        </div>
    </div>
    

    <h1> {{ $route.params.name }} </h1>

        <button type="button" class="btn btn-outline-danger mb-2" @click="volver"> Volver</button>
        <div class="card mb-3" style="max-width: 540px;">
            <div class="row g-0">
                <div class="col-md-4">
                    <img :src="img" class="img-fluid rounded-start" alt="...">
                </div>
                <div class="col-md-8">
                    <div class="card-body">
                        <h5 class="card-title">{{ nombre }}</h5>
                        <p class="card-text">This is a wider card with supporting text below as a natural lead-in to
                            additional
                            content. This content is a little bit longer.</p>
                        <p class="card-text"><small class="text-body-secondary">Last updated 3 mins ago</small></p>
                    </div>
                </div>
            </div>
        </div>
        <h1>{{ nombre }}</h1>
</template> -->
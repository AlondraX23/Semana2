<script setup>
import { ref } from 'vue';
import { useRouter, RouterLink } from 'vue-router';

let listaRegistros = ref([]);

const router = useRouter();

const login = ref({
    correo: '',
    password: ''
    
})
console.log(login)

function ingresar(event) {
    event.preventDefault()
    if ((listaRegistros.value.email == login.correo) && (listaRegistros.value.password == login.password)) {
        router.push('/contenido')
    } else {
        alert('Usuario o contraseña invalidos')
    }
}

fetch('https://raw.githubusercontent.com/LuisLaiton/API-json/main/usuarios.json')
    .then(res => res.json())
    .then((data) => {
        listaRegistros.value = data, 
        console.log(listaRegistros)
    })
</script>

<template>
    <div class="container py-4 main">
        <h1>Iniciar sesión</h1>
        <div>
            <form class="card p-4 bg-danger bg-opacity-25  border-0">
                <div class="row mb-3">
                    <label for="correoI" class="col-sm-2 col-form-label">Correo</label>
                    <div class="col-sm-10">
                        <input type="email" class="form-control" id="correoI" v-model="login.correo">
                    </div>
                </div>
                <div class="row mb-3">
                    <label for="passwordI" class="col-sm-2 col-form-label">Contraseña</label>
                    <div class="col-sm-10">
                        <input type="password" class="form-control" id="passwordI" v-model="login.password">
                    </div>
                </div>

                <div class="d-grid gap-2 d-md-flex justify-content-md-end">
                    <button type="submit" class="btn btn-primary" @click="ingresar">Ingresar</button>
                    <button type="reset" class="btn btn-dark">Borrar</button>
                </div>
            </form>
            <p class="text-center mt-2">
                <RouterLink to="/registro"
                    class="link-secondary link-offset-2 link-underline-opacity-25 link-underline-opacity-100-hovernav-link d-inline p-2">
                    ¿No tiene una cuenta? cree una</RouterLink>
            </p>
        </div>


    </div>
</template>

<style></style>
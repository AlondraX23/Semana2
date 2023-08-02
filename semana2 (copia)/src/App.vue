<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <nav class="navbar bg-body-tertiary text-white" data-bs-theme="dark">
    <div class="container-fluid">
      <RouterLink class="navbar-brand" to="/">
        <img
          src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/53/Pok%C3%A9_Ball_icon.svg/800px-Pok%C3%A9_Ball_icon.svg.png"
          alt="Logo" width="30" height="30" class="d-inline-block align-text-top">
        Home
      </RouterLink>
      <div class="navbar-nav-scroll">
        <RouterLink to="/contenido" class="nav-link d-inline p-2">Contenido</RouterLink>
        <RouterLink to="/registro" class="nav-link d-inline p-2">Registro</RouterLink>
        <RouterLink to="/login" class="nav-link d-inline p-2">Log in</RouterLink>
      </div>
    </div>
  </nav>

  <RouterView />
  <footer class="navbar bg-danger">
    <div class="container-fluid">
      <RouterLink class="nav-link text-white mx-auto" to="/">
        <img
          src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/53/Pok%C3%A9_Ball_icon.svg/800px-Pok%C3%A9_Ball_icon.svg.png"
          alt="Logo" width="30" height="30" class="d-inline-block text-center">
          &copy; 2023 · Alondra Damián
      </RouterLink>
    </div>
  </footer>
</template>

<style>
.main {
  min-height: 100vh;
  min-width: 1024px;
}
</style>

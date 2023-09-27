<script setup>
import { ref } from 'vue'
</script>

<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark border-bottom boder-body">
    <div class="container-fluid">
      <router-link class="navbar-brand" to="/" href="#">Cardapio</router-link>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbar">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <router-link class="nav-link" aria-current="page" to="/">Home</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" to="/about" href="#">About</router-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>
  <div class="main">
    <router-view></router-view>
  </div>

  <footer class="bg-dark text-light">
    <div>Bar {{ new Date().getFullYear() }}</div>
  </footer>
</template>

<style>
footer {
  position: fixed;
  bottom: 0%;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 56px;
}
</style>


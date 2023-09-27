<script setup>
import { ref } from 'vue'
let num = ref(0)
</script>

<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark border-bottom boder-body">
    <div class="container-fluid">
      <router-link class="navbar-brand" to="/" href="#">Cardapio</router-link>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
        arial-controls="navbar">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <router-link class="nav-link" arial-current="page" to="/" href="Home"></router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" to="/" href="#">About</router-link>
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
  height: 56%;
}
</style>


<script setup></script>

<template>
  <header class="app-header">
    <div class="logo">
      <img src="/src/assets/celerona.webp" width="150" alt="logo" />
    </div>
    <div class="content">
      <h1>Aplicación de Lista de Tareas</h1>
      <p>Organiza tus tareas diarias de manera eficiente</p>
    </div>
  </header>
</template>

<style scoped>
.app-header {
  display: flex;
  flex-direction: row;
  background-color: var(--primary-color);
  color: white;
}
.logo {
  width: 33%;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.content {
  width: 66%;
  padding: 20px;
}
</style>

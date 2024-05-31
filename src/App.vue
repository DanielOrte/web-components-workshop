<script setup>
import TodoList from './components/TodoList.vue'
import AppFooter from './templates/AppFooter.vue'
import AppHeader from './templates/AppHeader.vue'
import AppBody from './templates/AppBody.vue'
import { ref } from 'vue'
import BenefictsOfComponents from './components/FirstPart/BenefictsOfComponents.vue'

const simpleMode = ref(true)
</script>

<template>
  <button @click="simpleMode = !simpleMode">Toggle advanced mode</button>

  <div v-if="simpleMode">
    <BenefictsOfComponents></BenefictsOfComponents>
  </div>
  <div id="app" v-else>
    <AppHeader />
    <AppBody>
      <TodoList />
    </AppBody>
    <AppFooter />
  </div>
</template>

<style></style>

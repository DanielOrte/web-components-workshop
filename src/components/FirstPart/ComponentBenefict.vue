<script setup>
import { ref } from 'vue'

defineProps({
  titulito: String,
  fondito: String,
  colorcete: String
})

const emit = defineEmits(['pasadoPorEncima'])
const overTimes = ref(0)

function handleMouseEnter() {
  overTimes.value++
  emit('pasadoPorEncima', overTimes.value)
}
</script>

<template>
  <div
    class="card"
    :style="{ background: fondito, color: colorcete }"
    @mouseenter="handleMouseEnter()"
  >
    <h3>{{ titulito }}</h3>
    <h4>has pasado el raton por aqui {{ overTimes }} veces</h4>
    <slot></slot>
  </div>
</template>

<style scoped>
* {
  font-size: 20px;
  padding: 0;
  margin: 0 20;
}
</style>

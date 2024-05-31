<script setup lang="ts">
import ComponentBenefict from './ComponentBenefict.vue'

function showAlert(message) {
  alert(message)
}
</script>

<template>
  <ComponentBenefict
    titulito="Reutilización de Código"
    fondito="red"
    colorcete="blue"
    @pasado-por-encima="showAlert('Bienvenido al primer beneficio de los componentes')"
  >
    Los componentes pueden ser reutilizados en diferentes partes de la aplicación, lo que reduce la
    duplicación de código y facilita el mantenimiento.
  </ComponentBenefict>

  <ComponentBenefict
    titulito="Encapsulamiento"
    fondito="blue"
    colorcete="yellow"
    @pasado-por-encima="showAlert('Por aqui no queremos tu mouse, largo de aqui')"
  >
    Cada componente maneja su propio estado y lógica, lo que hace que el código sea más modular y
    fácil de entender.
  </ComponentBenefict>

  <ComponentBenefict titulito="Mantenimiento y Escalabilidad" fondito="yellow" colorcete="red">
    La modularidad de los componentes permite que varios desarrolladores trabajen en diferentes
    partes de la aplicación simultáneamente sin conflictos. También facilita la localización de
    errores y la adición de nuevas funcionalidades.
    <ComponentBenefict titulito="Anidamiento" colorcete="pink">
      Son anidables y eso es guachi
    </ComponentBenefict>
  </ComponentBenefict>
</template>

<style scoped></style>

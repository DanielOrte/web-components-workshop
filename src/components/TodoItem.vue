<script setup>
defineProps({
  task: {
    type: Object,
    required: true
  }
})

const emit = defineEmits(['delete', 'complete'])
</script>

<template>
  <li class="task" :class="{ completed: task.completed }">
    <!-- <input type="checkbox" :checked="task.completed" @change="emit('complete')" /> -->
    <div>
      <div>{{ task.label }}</div>
    </div>
    <!-- <button @click="emit('delete')">Borrar</button> -->
  </li>
</template>

<style scoped>
.task {
  border: var(--primary-color) 1px solid;
  margin: 15px;
  padding: 5px;
  border-radius: 5px;
}
/* .completed {
  text-decoration: line-through;
  color: grey;
} */
li {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0.5em 0;
}
</style>

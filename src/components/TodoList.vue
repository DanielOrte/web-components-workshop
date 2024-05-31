<script setup>
import { ref } from 'vue'
import TodoItem from './TodoItem.vue'

const newTask = ref('')
const tasks = ref([
  { label: 'Crear tareas', completed: false },
  { label: 'Eliminar tareas', completed: false },
  { label: 'Marcar tareas como completadas', completed: false },
  {
    label: 'Las tareas completadas deben aparecer tachadas',
    completed: false
  }
])

const addTask = () => {
  if (newTask.value.trim() === '') return
  tasks.value.push({
    label: newTask.value,
    completed: false
  })
  newTask.value = ''
}

const deleteTask = (index) => {
  tasks.value.splice(index, 1)
}

const complete = (index) => {
  tasks.value[index].completed = !tasks.value[index].completed
}
</script>

<template>
  <div class="todo-list">
    <h1>Lista de Tareas</h1>
    <input v-model="newTask" @keyup.enter="addTask" placeholder="Agregar nueva tarea" />
    <!-- <button @click="addTask">Agregar</button> -->
    <ul>
      <TodoItem v-for="(task, index) in tasks" :key="task.id" :task="task" />
      <!-- 
          @delete="deleteTask(index)"
        @complete="complete(index)"
       -->
    </ul>
  </div>
</template>

<style scoped></style>

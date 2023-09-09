<template>
  <div>
    <div v-for="task in tasks" id="card-item" :key="task.id">
        <div
        class="flex justify-between my-2 p-4 border rounded-md hover:border-slate-400"
        :class="[task.isDone ? 'border-red-300' : 'border-slate-300']">
          <div class="flex gap-3">
            <input :checked="task.isDone" type="checkbox" @click="task.isDone = !task.isDone"/>        
            <h2 :class="{ 'line-through italic': task.isDone }">{{ task.title }}</h2>
          </div>
          <h2>{{ task.category }}</h2>
        </div>
      </div>
    </div>
</template>

<script>
  export default {
    props: {
      tasks: {
        type: Array,
        required: true
      }
    }
  }
</script>
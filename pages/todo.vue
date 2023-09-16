<template>
  <div class="container px-5">
    <div class="flex justify-between">
      <h1 class="text-3xl">Todo List</h1>
      <div>
        <select
          v-model="category"
          class="p-2 border border-slate-300 rounded-md hover:border-slate-400 focus:outline-none focus:border-blue-500 appearance-none"
        >
          <option value="semua">semua</option>
          <option :value="true">selesai</option>
          <option :value="false">belum selesai</option>
        </select>
        <input
          v-model="search"
          type="text"
          class="p-2 border border-slate-300 rounded-md hover:border-slate-400"
        />
        <button class="p-2 btn-info rounded-md" @click="addTask = !addTask">
          Add Task
        </button>
      </div>
    </div>

    <ModalAddTaskVue v-if="addTask" @close="addTask = false"></ModalAddTaskVue>

    <taskItem :tasks="filterResult"></taskItem>
  </div>
</template>

<script>
import ModalAddTaskVue from '~/components/ModalAddTask.vue'
import taskItem from '~/components/taskItem.vue'

export default {
  components: {
    taskItem,
    ModalAddTaskVue,
  },
  data() {
    return {
      tasks: [
        {
          id: 1,
          title: 'Belajar',
          isDone: false,
        },
        {
          id: 2,
          title: 'Tidur',
          isDone: false,
        },
        {
          id: 3,
          title: 'Main game',
          isDone: false,
        },
      ],
      search: '',
      category: 'semua',
      addTask: false,
    }
  },
  computed: {
    filterResult() {
      if (this.search) {
        return this.tasks.filter((item) => {
          return this.search
            .toLowerCase()
            .split(' ')
            .every((v) => item.title.toLowerCase().includes(v))
        })
      } else if (this.category !== 'semua') {
        return this.tasks.filter((task) => task.isDone === this.category)
      }
      return this.tasks
    },
  },

  // mounted() {
  //   console.log(this.filterResult)
  // },
}
</script>

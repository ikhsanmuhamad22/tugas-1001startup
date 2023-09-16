<template>
  <div
    class="modal fixed w-full h-full top-0 left-0 flex items-center justify-center"
  >
    <div
      class="modal-overlay absolute w-full h-full bg-gray-900 opacity-50"
    ></div>
    <div
      class="modal-container bg-white w-11/12 md:max-w-md mx-auto rounded shadow-lg z-50 overflow-y-auto"
    >
      <div class="modal-content py-4 text-left px-6">
        <form class="p-6" @submit.prevent="tambahTask">
          <h1 class="text-2xl font-semibold mb-4">Add Task</h1>
          <div class="mb-4">
            <label for="title" class="block text-gray-700 font-medium mb-2"
              >Task:</label
            >
            <input
              id="title"
              v-model="task.title"
              type="text"
              name="title"
              class="w-full px-4 py-2 border rounded-md focus:outline-none focus:border-blue-500"
              placeholder="Add your task"
            />
          </div>
          <div class="mb-4">
            <label for="category" class="block text-gray-700 font-medium mb-2"
              >category:</label
            >
            <select
              id="category"
              v-model="task.isDone"
              name="category"
              class="w-full px-4 py-2 border rounded-md focus:outline-none focus:border-blue-500"
            >
              <option :value="false">belum selesai</option>
              <option :value="true">selesai</option>
            </select>
          </div>
          <div class="text-end">
            <button
              class="bg-red-500 hover:bg-red-700 text-white font-bold py-2 px-4 rounded"
              @click="$emit('close')"
            >
              Close
            </button>
            <button
              type="submit"
              class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded"
            >
              Submit
            </button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    tasks: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {
      task: {
        title: '',
        isDone: false,
      },
    }
  },
  methods: {
    tambahTask() {
      this.$emit('input-task', this.task)
      this.$emit('close')
    },
  },
}
</script>

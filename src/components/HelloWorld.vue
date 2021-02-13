<template>
  <div class="flex flex-col bg-white rounded shadow p-4 w-full max-w-xs">
    <h1 class="font-bold text-gray-700 text-center pb-4">{{ msg }}</h1>
    <button
        class="block px-4 py-2 transition duration-100 ease-in-out focus:border-blue-500 focus:ring-2 focus:ring-blue-500 focus:outline-none focus:ring-opacity-50 disabled:opacity-50 disabled:cursor-not-allowed text-white bg-blue-500 border border-transparent shadow-sm rounded hover:bg-blue-600"
        @click="count++">count is: {{ count }}</button>
  </div>
</template>

<script lang="ts">
import { ref, defineComponent } from 'vue'
export default defineComponent({
  name: 'HelloWorld',
  props: {
    msg: {
      type: String,
      required: true
    }
  },
  setup: () => {
    const count = ref(0)
    return { count }
  }
})
</script>

<style scoped>

</style>

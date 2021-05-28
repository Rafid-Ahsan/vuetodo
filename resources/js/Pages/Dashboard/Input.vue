<template>
  <div class="mt-1">
    <form @submit.prevent="submit">
      <input
        @keyup.enter="submit"
        v-model="form.name"
        type="text"
        class="shadow-sm focus:ring-indigo-500 focus:border-indigo-500 block w-full sm:text-sm border-gray-300 rounded-md"
        placeholder="Write your Todo Here"
      />
    <p class="text-red-600">{{ $page.props.errors.todo }}</p>

      <!-- <p v-if="errors.name">{{ errors.name }}</p> -->
    </form>
  </div>
</template>

<script>
import { reactive } from 'vue'
import { Inertia } from '@inertiajs/inertia'

export default {
  setup () {
    const form = reactive({
      name: null
    })

    function submit() {
      Inertia.post('/todos', form)
    }

    return { form, submit }
  },
};
</script>

<style scoped>
</style>

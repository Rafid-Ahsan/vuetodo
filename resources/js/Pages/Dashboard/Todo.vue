<template>
  <!-- This example requires Tailwind CSS v2.0+ -->
  <div class="bg-white shadow overflow-hidden sm:rounded-md">
    <p class="text-green-600 alert" v-if="$page.props.flash.success">
      {{ $page.props.flash.success }}
    </p>
    <ul class="divide-y divide-gray-200">
      <li v-for="todo in todos.data" :key="todo.id">
        <SingleTodo :todo="todo" />
      </li>
    </ul>
  </div>
</template>

<script>
import SingleTodo from "./SingleTodo";

export default {
  props: ["todos"],
  components: {
    SingleTodo,
  },
};
</script>
<style scoped>
</style>

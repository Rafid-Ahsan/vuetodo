<template>
  <app-layout>
    <div class="py-12 px-12">
      <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
        <div class="bg-white overflow-hidden shadow-xl sm:rounded-lg">
          <div class="p-12">
            <div class="bg-white">
              <div class="max-w-7xl mx-auto py-12 lg:py-16 text-center">
                <h2
                  class="inline text-3xl font-extrabold tracking-tight text-gray-900 sm:block sm:text-4xl"
                >
                  Write More Todo!
                  <span class="text-indigo-600">Make your life Easier</span>
                </h2>
              </div>
            </div>
            <Input />
            <Todo :todos="todos"/>
          </div>
        </div>
      </div>
    </div>
  </app-layout>
</template>

<script>
import AppLayout from "@/Layouts/AppLayout";
import Welcome from "@/Jetstream/Welcome";
import Input from '../Pages/Dashboard/Input';
import Todo from '../Pages/Dashboard/Todo';

export default {
  components: {
    AppLayout,
    Welcome,
    Input,
    Todo
  },
  props: ['todos']
};
</script>

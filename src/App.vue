<template>
  <div id='app'>
    <h1>To-do List</h1>
    <ToDoForm></ToDoForm>
    <ul>
      <li v-for="item in ToDoItems" :key="item.id">
        <ToDoItem :label="item.label" :done="item.done" :id="item.id"></ToDoItem>
      </li>
    </ul>
  </div>
</template>

<script>
import { nanoid } from "nanoid";
import ToDoItem from './components/ToDoItem.vue';
import ToDoForm from "./components/ToDoForm.vue";
export default {
  name: 'App',
  components: {ToDoItem, ToDoForm,},

  data() {
    return {
      ToDoItems: [
        { label: "Learn Vue", done: false, id: 'todo-' + nanoid()},
        { label: "Create a Vue project with the CLI", done: true, id: 'todo-' + nanoid()},
        { label: "Have fun", done: true, id: 'todo-' + nanoid()},
        { label: "Create a to-do list", done: false, id: 'todo-' + nanoid()},
        { label: "MDN 3 pages learned", done: false, id: 'todo-' + nanoid()},
        { label: "MDN more than half learned", done: false, id: 'todo-' + nanoid()},
        { label: "MDN Learned all", done: false, id: 'todo-' + nanoid()},
        { label: "Start another practice", done: false, id: 'todo-' + nanoid()},
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  ul {list-style-type: none;}
}
</style>
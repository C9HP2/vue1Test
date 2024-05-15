<template>
<form @submit.prevent="onSubmit">
  <label for="new-todo-input">THE LABEL</label>
  <input type="text" id="new-todo-input" 
  name="new-todo" autocomplete="off" 
  v-model="label" />
  <button type="submit">Add</button>
</form>
</template>
<script>
export default {
  data() {
    return {
      label: '',
    }
  },
  methods: {
    onSubmit() {
      console.log("THE LABEL VALUE: ", this.label)
    }
  }
};
</script>

<template>
<form @submit.prevent="onSubmit">
  <h2 class="label-wrapper"> 
    <label for="new-todo-input" class="lebel-lg">What needs to be done?</label>
  </h2>

  
  <input 
    type="text" id="new-todo-input" name="new-todo" 
    autocomplete="off" v-model.trim.lazy="label" 
    class="input__lg"
  />
  <button class="btn btn__primary btn__lg" type="submit">Add</button>
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
      if (this.label === "" | this.label) {return;} // empty todo label not allowed
      this.$emit("todo-added", this.label);
      this.label = "";
    }
  }
};
</script>

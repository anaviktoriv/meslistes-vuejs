<template>
  <div class="todo-item-background d-flex align-items-center m-1">
<div class="d-flex align-items-center">
    <div class=" p-2" v-on:click="markComplete">
      <img v-if="todo.completed" :src="fullCircle" class="circle-icon m-1" alt="circle" />
      <img v-else :src="emptyCircle" class="circle-icon m-1" alt="circle" />
    </div>
    <p class="m-1 p-0 open-sans-light" v-bind:class="{'is-completed':todo.completed}">{{todo.title}}</p>
  </div>
<button class="btn rose-button ml-auto p-2"> <img class="button-image" src="../assets/edit-icon.svg" alt=""> </button>
<button class="btn red-button p-2"> <img class="button-image" src="../assets/trash-icon.svg" alt=""> </button>
</div>
</template>

<script>
export default {
  name: "TodoItem",
  props: ["todo"],
  methods: {
    markComplete() {
      this.todo.completed = !this.todo.completed;
    },
  },
  data() {
    return {
      emptyCircle: require("../assets/empty-black-circle.svg"),
      fullCircle: require("../assets/full-gray-circle.svg")
    };
  },
};
</script>

<style scoped>
.btn:focus,.btn:active {
   outline: none !important;
   box-shadow: none;
}
.todo-item-background{
background-color: #FFFFFF;
}
.open-sans-light{
font-family: 'Open Sans', sans-serif;
font-size: 20px;
}

.is-completed {
color: #D3D3D3;
  text-decoration: line-through;
}
.circle-icon {
  width: 18px;
  height: auto;
}
.button-image{
height: 35px;
width: auto;
}
.rose-button{
border-radius: 0;
background-color: rgba(240, 214, 226, 1);
}
.rose-button:active, .rose-button:hover, .rose-button:focus{
background-color: rgba(214, 191, 202, 1);
}
.red-button{
border-radius: 0;
background-color: rgba(242, 93, 97, 1);
}
.red-button:active, .red-button:hover, .red-button:focus{
background-color: rgba(214, 84, 88, 1);
}
</style>
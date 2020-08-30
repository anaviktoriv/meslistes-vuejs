<template>
  <div class=" d-flex flex-column background-color col-4 no-gutters m-0 p-0">
<h1 class="text-center open-sans-regular mt-2">Lists</h1>
<img class="icon mx-auto m-2 p-1" src="../assets/plus-icon.svg" alt="plus-icon" @click="makeAddNewListVisible">
<div :class="{invisible: addNewListViewIsInvisible}">
<addNewList/>
</div>
    <div v-for="list in lists" :key="list.id">
      <List v-bind:list="list" />
    </div>
  </div>
</template>

<script>
import List from "./List.vue"
import AddNewList from "./AddNewList"
export default {
  name: "Lists",
  components: {
    List,
AddNewList
  },
  props: ["lists"],
data(){
return{
addNewListViewIsInvisible: true
}
},
methods: {
makeAddNewListVisible(){
this.addNewListViewIsInvisible = false
}
}
};
</script>

<style scoped>
.background-color {
  background-color: #ffffff;
  height: 100vh;
}

.open-sans-regular {
  font-family: "Open Sans", sans-serif;
font-weight: 600;
  font-size: 26px;
  text-transform: uppercase;
}
.icon {
  height: 40px;
  width: auto;
}
.icon:hover, .icon:focus, .icon:active{
background-color: #f5f2f2;
border-radius: 6px;
}
.invisible{
display: none;
}
</style>
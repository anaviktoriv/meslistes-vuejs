<template>
  <div class="d-flex align-items-center list-background">
    <div class="d-flex align-items-center m-1 ml-3">
      <img class="icon" :src="list.icon" alt />
      <p
        class="m-1 p-2 open-sans-light"
        v-bind:class="{'is-completed':list.completed}"
        v-on:click="showItems"
      >{{list.title}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "List",
  props: ["list"],
  methods: {
    showItems() {
      console.log('Showing Items')
    },
  },
};
</script>

<style scoped>

.open-sans-light {
  font-family: "Open Sans", sans-serif;
  font-size: 20px;
  text-transform: uppercase;
}

.is-completed {
  color: #d3d3d3;
  text-decoration: line-through;
}
.icon {
  height: 35px;
  width: auto;
}
.list-background{
background-color: #ffffff;
}
.list-background:focus, .list-background:active, .list-background:hover{
background-color: #f5f2f2;
}
</style>
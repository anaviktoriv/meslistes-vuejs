<template>
  <div id="app" class="app-background">
    <div class="row m-1">
      <Lists v-bind:lists="lists" />
      <Todos v-bind:todos="todos" />
    </div>
  </div>
</template>

<script>
import Todos from "./components/Todos";
import Lists from "./components/Lists";
export default {
  name: "App",
  components: {
    Todos,
    Lists,
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: "Todo One",
          completed: false,
        },

        {
          id: 2,
          title: "Todo Two",
          completed: true,
        },

        {
          id: 3,
          title: "Todo Three",
          completed: false,
        },
      ],
      lists: [
        {
          id: 1,
          title: "List One",
          completed: false,
          icon: require("./assets/listIcons/bag-icon.svg"),
          items: [
            {
              id: 1,
              title: "Todo One",
              completed: false,
            },

            {
              id: 2,
              title: "Todo Two",
              completed: true,
            },

            {
              id: 3,
              title: "Todo Three",
              completed: false,
            },
          ],
        },

        {
          id: 2,
          title: "List Two",
          completed: true,
          icon: require("./assets/listIcons/plane-icon.svg"),
          items: [
            {
              id: 1,
              title: "Todo One",
              completed: false,
            },

            {
              id: 2,
              title: "Todo Two",
              completed: true,
            },

            {
              id: 3,
              title: "Todo Three",
              completed: false,
            },
          ],
        },

        {
          id: 3,
          title: "List Tree",
          completed: false,
          icon: require("./assets/listIcons/book-icon.svg"),
          items: [
            {
              id: 1,
              title: "Todo One",
              completed: false,
            },

            {
              id: 2,
              title: "Todo Two",
              completed: true,
            },

            {
              id: 3,
              title: "Todo Three",
              completed: false,
            },
          ],
        },
      ],
    };
  },
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.4;
}

.app-background {
  height: 100vh;
  width: auto;
  background-image: url("assets/background-light.jpg");
  background-repeat: no-repeat;
  background-size: cover;
}
</style>

<template>
  <div class="add-new-list-container mx-auto d-flex flex-column align-items-center mb-2">
    <input class="list-name-input mt-2 mb-2 pl-1" type="text" placeholder="Name your new list..." />
    <div class="d-flex flex-wrap icon-container mx-auto mb-2">
        <img class="list-icon"  v-for="icon in icons" :key="icon.id" :src="icon.link" alt />
    </div>
<div class="button-wrapper">
<button class="btn transparent-button transparent-button-left">Cancel</button>
<button class="btn transparent-button transparent-button-right">OK</button>
</div>
  </div>
</template>

<script>
export default {
  name: "AddNewList",

  data() {
    return {
      defaultIcon: {
        id: 7,
        name: "circle",
        link: require("../assets/listIcons/circle-icon.svg"),
      },

      icons: [
        {
          id: 1,
          name: "bag",
          link: require("../assets/listIcons/bag-icon.svg"),
        },

        {
          id: 2,
          name: "plane",
          link: require("../assets/listIcons/plane-icon.svg"),
        },

        {
          id: 3,
          name: "clothes",
          link: require("../assets/listIcons/clothes-icon.svg"),
        },

        {
          id: 4,
          name: "cooking",
          link: require("../assets/listIcons/cooking-icon.svg"),
        },

        {
          id: 5,
          name: "book",
          link: require("../assets/listIcons/book-icon.svg"),
        },

        {
          id: 6,
          name: "check",
          link: require("../assets/listIcons/check-icon.svg"),
        },

        {
          id: 7,
          name: "sport",
          link: require("../assets/listIcons/sport-icon.svg"),
        },

        {
          id: 8,
          name: "gift",
          link: require("../assets/listIcons/gift-icon.svg"),
        },

        {
          id: 9,
          name: "house",
          link: require("../assets/listIcons/house-icon.svg"),
        },

        {
          id: 10,
          name: "sport",
          link: require("../assets/listIcons/house-icon.svg"),
        },

        {
          id: 11,
          name: "star",
          link: require("../assets/listIcons/star-icon.svg"),
        },

        {
          id: 12,
          name: "bulb",
          link: require("../assets/listIcons/bulb-icon.svg"),
        },
      ],
    };
  },
};
</script>

<style scoped>

.list-icon{
width: 46px;
height: 46px;
padding: 3px;
}

.list-icon:hover, .list-icon:active, .list-icon:focus{
background-color: white;
}

.icon-container{
width: 184px;
}
.add-new-list-container{
width: 210px;
height: auto;
background-color: #f5f2f2;
border-radius: 6px;
}
.list-name-input{
border: solid 1px#adadad;
  font-family: "Open Sans", sans-serif;
  font-size: 16px;
}

::-webkit-input-placeholder { /* Chrome/Opera/Safari */
  color: #adadad;
}
::-moz-placeholder { /* Firefox 19+ */
  color:#adadad;
}
:-ms-input-placeholder { /* IE 10+ */
  color: #adadad;
}
:-moz-placeholder { /* Firefox 18- */
  color: #adadad;
}

.button-wrapper{
width: 100%;
border-top: solid 1px #adadad;
}
.transparent-button{
width: 50%;
border-radius: 0;
}
.transparent-button:hover, .transparent-button:focus, .transparent-button:active{
background-color: #e6e3e3;
}

.transparent-button-left{
width: 50%;
border-right: solid 0.5px #adadad;
border-radius: 0 0 0 6px;
}

.transparent-button-right{
border-radius: 0 0 6px 0;
}



.btn:focus,.btn:active {
   outline: none !important;
   box-shadow: none;
}
</style>

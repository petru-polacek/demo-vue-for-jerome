<template>
  <div id="app">
    <img alt="Vue logo" src="https://vuejs.org/images/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
  },

  data() {
    return {
      vm: {
        castel: {
          name: "Caster of Jérôme!",
        },
        rooms: [
          { name: "room1", color: "red" },
          { name: "room2", color: "green" },
          { name: "room3", color: "blue" },
        ],
      },
    };
  },

  mounted() {
    console.log("Hello Jérôme!");
    console.log("Please create an object that have a property an array");
    console.log("Please iter over all properties and over all values");

    var myObj = this.vm;

    console.log(" my obj ", myObj);

    console.log(" Castel of Jérôme has ", myObj.rooms.length, " room");
    console.log(" Castel of Jérôme has ", myObj.rooms, " room");

    console.log("Room 1 ", myObj.rooms[0]);
    console.log("Room 2 ", myObj.rooms[1]);
    console.log("Room 3 ", myObj.rooms[2]);

    for (let index = 0; index < myObj.rooms.length; index++) {
      console.log("Room  en° " + index + " is : ", myObj.rooms[index]);
    }

    console.log("This is done!");
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
}
</style>

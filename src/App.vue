<template>
  <div id="app" class="borderBold">
    Hi, {{name_first}}!
    <navigation-link url="https://www.vuejs-seminar.de">
    <template v-slot:image>
      <img src="https://d10s7cl4nxfjv3.cloudfront.net/wp-content/uploads/sites/2/2019/09/vuejs-schulung-inhouse-logo.png"
      style="height:20px"/>
    </template>
    Zum Profil
    </navigation-link>
    <TodoList/>
    </div>
</template>

<script>
import TodoList from "./components/TodoList";
import NavigationLink from "./components/NavigationLink.vue";
export default {
  name: "App",
  data: () => ({
    name_first: 'Lennox Elijah',
  }),
  components: {
    TodoList,
    NavigationLink
  },
  methods: {
    test(){
      alert("Hallo");
    },
    test2(){
      alert("adios");
    }
  }
};
</script>
<style>
.borderBold {
  border: 1px solid black;
  margin: 5px;
  padding: 5px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

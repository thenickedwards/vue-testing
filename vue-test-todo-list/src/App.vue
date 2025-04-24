<template>
  <div id="app">
    <h1>{{ title }}</h1>
    <h2><em>Todo List via Vue.js + Typescript</em></h2>
    <TodoInput />
    <!-- {{ $store.state.todos }} -->
      <!-- OR USE COMPONENT-->
    <TodoList />
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import TodoList from './components/TodoList.vue';
import TodoInput from './components/TodoInput.vue';

@Options({
  components: {
    TodoInput,
    TodoList
  },
})
export default class App extends Vue {
  public title = 'Hello World from Nick Edwards!';
  // Lifecycle example
  public mounted() {
    console.log('App mounted!')
  }

}
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

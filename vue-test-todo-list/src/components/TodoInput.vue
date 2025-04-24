<template>
    <form @submit.prevent="addTodo" class="todo-iput">
        <input type="text" v-model="newTodo" />
        <input type="submit" value="Add Todo" />

    </form>
</template>

<script lang="ts">
import { Vue } from 'vue-class-component';
import store from '../store';

export default class TodoInput extends Vue {
    public newTodo = '';

    public addTodo(): void {
        store.dispatch('addTodo', this.newTodo);
        // clear input
        this.newTodo = '';
    }
}
</script>

<!-- <style>
</style> -->
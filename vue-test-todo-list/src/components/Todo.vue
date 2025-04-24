<template>
    <div class="todo">
        <span v-text="todo"></span>
        <button @click="deleteTodo">X</button>
    </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

@Options({
    props: ['todo'],
    methods: {
        deleteTodo(): void {
            this.$store.dispatch('deleteTodo', this.todo);
        }
    }
})

export default class Todo extends Vue {}
</script>

<style>
.todo {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 12px 24px;
    border-bottom: 1px solid #ccc;
}
</style>
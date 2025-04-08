<script setup>
import NewButton from './components/newButton.vue';
import NewButton2 from './components/newButton2.vue';
import { ref } from 'vue'
const count = ref(0)
const countUp = () => {
  count.value++
}
const countDown = () => {
  count.value--
}
</script>


<template>
  <div>
    <h1>Hello World from Nick Edwards!</h1>
    <p>Vue Test 2</p>
    <br />
    <NewButton2 @click=countUp>Click me to increment!</NewButton2>
    
    <div>
      {{ count }}
    </div>
    <NewButton2 style="background-color: crimson;" @click=countDown>Click me to decrement!</NewButton2>
  </div>
</template>


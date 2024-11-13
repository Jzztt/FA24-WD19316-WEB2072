<template>
  <div>
    <div><h3>Event Binding</h3></div>
    <div>
      <p>Count: {{ count }}</p>
      <!-- inline event -->
      <button class="btn btn-primary" @click="count++">Increase</button>
      <!-- method event -->
      <!-- <button class="btn btn-primary" @click="increment">Increase</button> -->
      <!--  method event with parameter -->
      <button class="btn btn-primary" @click="increment(2)">Increase 2</button>
      <button class="btn btn-primary" @click="increment(5)">Increase 5</button>
    </div>
    <div>
      <!-- stop propagation -->
      <button @click.stop="console.log('button1')">
        Button1
        <button @click.stop="console.log('button2')">button 2</button>
      </button>
    </div>
    <div>
      <!--  prevent default -->
      <form action="">
        <label for=""></label>
        <input type="text" v-model="inputRef" />
        <button type="submit" @click.prevent="console.log(inputRef)">
          Login
        </button>
      </form>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const inputRef = ref('')

const count = ref(0)
const increment = param => {
  count.value += param
}
</script>

<style lang="scss" scoped>
</style>
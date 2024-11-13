<template>
  <div>
    <div>
      <h3>LIST RENDERING</h3>
    </div>
    <div>
      <h3>V-for</h3>
      <ul v-for="(food, index) in foods" :key="food">
        <li>{{ index }} - {{ food }}</li>
      </ul>
    </div>
    <div>
      <h3>v-for object</h3>
      <ul v-for="(value, key) in user" :key="key">
        <li>{{ key }}-{{ value }}</li>
      </ul>
    </div>
    <div>
      <h3>v-for with destructuring</h3>
      <ul v-for="{ id, name, address } in students" :key="id">
        <li v-if="name === 'John'">{{ id }} - {{ name }} - {{ address }}</li>
      </ul>
    </div>
  </div>
</template>

<script setup>
import { reactive } from 'vue'

const foods = reactive(['rice', 'noodle', 'pizza'])

const user = reactive({
  name: 'John',
  age: 18,
  abc: 'demo',
})

const students = reactive([
  {
    id: 1,
    name: 'John',
    address: 'Mỹ Đình',
  },
  {
    id: 2,
    name: 'Merry',
    address: 'Cam ranh',
  },
])
</script>

<style lang="scss" scoped>
</style>
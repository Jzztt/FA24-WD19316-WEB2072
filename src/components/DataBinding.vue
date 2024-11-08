<template>
  <div>
    <p :class="active" :style="styles">{{ name }}</p>

    <input type="text" v-model="name" />
  </div>
</template>

<script setup>
import { reactive, ref } from 'vue'

const name = ref('LVH')
const active = ref('active')
const styles = reactive({
  color: 'red',
  fontSize: '20px',
  background: 'blue',
})
</script>

<style scoped>
.active {
  color: red;
}
</style>
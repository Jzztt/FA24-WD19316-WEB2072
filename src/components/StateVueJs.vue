<template>
  <div>
    Trạng Thai : {{ notification }}
    <button @click="changeNotification">Online</button>
  </div>
</template>


<script setup>
import { ref } from 'vue'

const notification = ref('offline')
const changeNotification = () => {
  notification.value = 'online'
}
</script>

<style lang="scss" scoped>
</style>
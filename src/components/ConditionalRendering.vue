<template>
  <div>
    <div>
      <h1>Conditional Rendering</h1>
      <p v-show="isActive">System is Active</p>
      <p v-show="!isActive">System is unActive</p>
    </div>

    <div>
      <p v-if="user.age > 30">{{ user.name }} là Trung niên</p>
      <p v-else-if="user.age >= 18">{{ user.name }} là Thanh niên</p>
      <p v-else>{{ user.name }} là Thiếu niên</p>
    </div>

    <div>
      <h3>Bài tập</h3>
      <p v-show="isVisible">Thông báo 1</p>
      <p v-show="!isVisible">Thông báo 2</p>
      <button class="btn btn-primary" @click="handleChangeStatus">
        Change status
      </button>
    </div>
  </div>
</template>

<script setup>
import { reactive, ref } from 'vue'

const isActive = ref(true)
const isVisible = ref(true)

const user = reactive({
  name: 'John Doe',
  age: 18,
})

const handleChangeStatus = () => {
  isVisible.value = !isVisible.value
}
</script>

<style lang="scss" scoped>
</style>
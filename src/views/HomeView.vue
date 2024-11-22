<script setup>
import TableComponent from '@/components/TableComponent.vue';
import instanceAxios from '@/utils/configAxios';
import { onMounted, provide, ref } from 'vue';

const students = ref([

])
const title = ref("HomeViews")
const message = ref("Hello world")
// truyền dữ liệu title qua provide
provide('title', title.value)
const deleteItem = (id) => {
  students.value = students.value.filter((student) => student.id !== id)
}




const fetchStudents = async () => {
  const fetchStudentsResponse = await instanceAxios.get('students')
  console.log(fetchStudentsResponse);
  students.value = fetchStudentsResponse.data
}

onMounted(() => {
  fetchStudents()
})


</script>

<template>
  <main>
    <TableComponent :msg="message" :students="students" @deleteStudents="deleteItem" />
  </main>
</template>

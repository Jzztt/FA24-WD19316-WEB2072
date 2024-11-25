<template>
    <div>
        <!-- Button trigger modal -->
        <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#exampleModal">
            Create Student
        </button>

        <!-- Modal -->
        <div class="modal fade"  id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
            <div class="modal-dialog modal-dialog-centered">
                <div class="modal-content">
                    <form @submit.prevent="handleSubmit">
                        {{ student }}
                        <div class="modal-header">
                            <h1 class="modal-title fs-5" id="exampleModalLabel">Modal Create Student</h1>
                            <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                        </div>
                        <div class="modal-body">
                            <div class="form-group">
                                <label for="name">Name</label>
                                <input type="text" id="name" class="form-control" placeholder="Enter Name" v-model="student.name">
                            </div>
                            <div class="form-group">
                                <label for="mssv">Mssv</label>
                                <input type="text" id="mssv" class="form-control" placeholder="Enter Mssv" v-model="student.mssv">
                            </div>
                        </div>
                        <div class="modal-footer">
                            <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
                            <button type="submit" class="btn btn-primary" >Save changes</button>
                        </div>
                    </form>
                </div>
            </div>
        </div>

    </div>
</template>

<script setup>
import { ref } from 'vue';

const emit = defineEmits(['submitForm'])
const student = ref({
    name: '',
    mssv : ''
})

const handleSubmit =  () => {
   emit('submitForm', student.value)
}

</script>

<style lang="scss" scoped></style>
<template>
    <div>
        <div>
            <h3>Form Binding</h3>
        </div>
        <form action="">
            <div class="form-group">
                <!-- type="text" -->

                <label for="email">Email</label>
                <input type="text" v-model="email">
            </div>
            <div class="form-group">
                <!-- type="multi text" -->
                <label for="contact">Contact</label>
                <textarea placeholder="Please enter contact" v-model="contact"></textarea>
            </div>
            <div class="form-group">
                <!--  type = "checkbox" -->
                <label for="term">Term</label>
                <input type="checkbox" v-model="isChecked">
            </div>
            <!-- multi checkbox -->
            <div class="form-group">
                <label for="html">HTML</label>
                <input type="checkbox" value="html" v-model="courseName">
            </div>
            <div class="form-group">
                <label for="css">Css</label>
                <input type="checkbox" value="css" v-model="courseName">
            </div>
            <!--  select option -->
            <div class="form-group">
                <label for="course">Course</label>
                <select name="course" id="course" v-model="course">
                    <option value="html">HTML</option>
                    <option value="javascript">Javascript</option>
                </select>
            </div>
            <!-- radio -->
             <div class="form-group">
                <label for="gender">Gender</label>
                <input type="radio" value="male" v-model="gender">
                <label for="male">Male</label>
                <input type="radio" value="female" v-model="gender">
                <label for="female">Female</label>
             </div>
            <p>{{ email }}</p>
            <p>{{ contact }}</p>
            <p>{{ isChecked }}</p>
            <p>{{ courseName }}</p>
            <p>{{ course }}</p>
            <p>{{ gender }}</p>





        </form>

    </div>
</template>

<script setup>
import { ref } from 'vue';

const email = ref('')
const contact = ref('')
const isChecked = ref(false)
const courseName = ref([])
const course = ref('')
const gender = ref('')
</script>

<style lang="scss" scoped></style>
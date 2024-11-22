<template>
    <div>
        <div>
            <h3>{{ message }}</h3>
            <button class="btn btn-primary" @click="handleChange">Change Message</button>
        </div>

    </div>
</template>

<script setup>
import { onMounted, onUnmounted, onUpdated, ref } from 'vue';

const message = ref('Hello world')

const handleChange = () => {
    message.value = "Life Cycle"
}

console.log('created');

onMounted(()=> {
    console.log('mounted');

})

onUpdated(()=> {
    console.log('updated');
})

onUnmounted(()=> {
    console.log('unmounted');
})


</script>

<style lang="scss" scoped>

</style>
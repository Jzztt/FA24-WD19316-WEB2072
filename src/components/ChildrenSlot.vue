<template>
    <div>
        <!-- <slot name="header"></slot>
        <slot></slot>
        <slot name="footer"></slot> -->
        <slot :mes = "message"></slot>

    </div>
</template>

<script setup>
const message = 'Gửi dữ liệu từ children slot'

</script>

<style lang="scss" scoped></style>
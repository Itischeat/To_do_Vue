<template>
    <button class="btn">
        <slot></slot>
    </button>
</template>

<script>
export default {
    name: 'MyButton',
}
</script>

<style scoped>
.btn {
    color: teal;
    width: 100px;
    height: 30px;
    background: none;
    border: 1px solid teal;
}
</style>
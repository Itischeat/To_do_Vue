<template>
    <div class="posts">
        <div>
            <div><strong>Название:</strong> {{ post.title }}</div>
            <div><strong>Описание:</strong> {{ post.body }}</div>
        </div>

    </div>
</template>

<script>

export default {

    props: {
        post: {
            type: Object,
            required: true,
        }
    }
}
</script>

<style scoped>
.posts {
    padding: 15px;
    border: 2px teal solid;
    margin-top: 10px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}
</style>
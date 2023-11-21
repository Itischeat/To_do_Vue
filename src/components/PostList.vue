<template>
    <div class="wrapper">
        <h3>Список</h3>
        <PostItem :post="post" class="posts" v-for="post in posts"></PostItem>
    </div>
</template>

<script>
import PostItem from '@/components/PostItem.vue';

export default {
    props: {
        posts: {
            type: Array,
            required: true,
        }
    },
    components: { PostItem }
}
</script>

<style scoped>
.wrapper {
    padding: 20px;
}
</style>
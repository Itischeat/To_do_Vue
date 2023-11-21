<template>
    <div class="app">
        <PostForm @create="createPost"></PostForm>
        <PostList :posts="posts"></PostList>
    </div>
</template>

<script>
import PostForm from '@/components/PostForm.vue';
import PostList from '@/components/PostList.vue';
export default {
    components: {
        PostList, PostForm
    },
    data() {
        return {
            posts: [
                { id: 1, title: 'JS', body: 'Описание' },
                { id: 2, title: 'JS2', body: 'Описание 2' },
                { id: 3, title: 'JS3', body: 'Описание 3' },
            ],
        }
    },
    methods: {
        createPost(post) {
            this.posts.push(post);
        },
    },
}
</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
</style>
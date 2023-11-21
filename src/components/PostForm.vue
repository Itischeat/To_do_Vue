<template>
    <form @submit.prevent>
        <h4>Создание элемента</h4>
        <my-input v-model="post.title" placeholder="Название"></my-input>
        <my-input v-model="post.body" placeholder="Описание"></my-input>
        <MyButton style="align-self: flex-end;" @click="createPost">Создать!</MyButton>
    </form>
</template>

<script>

export default {
    data() {
        return {
            post: {
                title: '',
                body: '',
            },
        }
    },
    methods: {
        createPost() {
            this.post.id = Date.now();
            this.$emit('create', this.post);
            this.post = {
                title: '',
                body: '',
            }
        }
    }
}
</script>

<style scoped>
form {
    padding: 20px;
    display: flex;
    flex-direction: column;

}

form>* {
    margin-top: 15px;
}

form>h4 {
    text-align: center;
    font-size: 18px;
}
</style>
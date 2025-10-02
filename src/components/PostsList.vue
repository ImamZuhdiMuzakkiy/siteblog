<template>
    <div class="post-list">
        <div v-for="post in posts" :key="post.id" class="post-item">
            <PostSingle :post="post" />
        </div>
    </div>
</template>

<script>
import PostSingle from './PostSingle.vue'
export default {
    props: [
        'posts'
    ],
    components: { PostSingle },
    setup(props) {
        console.log(props.posts);
        return { props }
    }
}
</script>

<style>

</style>
<template>
  <div class="home">
    <h1>Home</h1>
    <PostList :posts="posts" />
  </div>
</template>

<script>
import PostList from '../components/PostsList.vue'
import getPosts from '../composable/getPosts.js'

export default {
  name: 'HomeView',
  components: { PostList },
  setup() {
    const { posts, error, load } = getPosts()

    load()

    return { posts, error }
  },
  
}
</script>

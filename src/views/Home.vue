<template>
    <h1>Featured Posts</h1>
    <PostList :posts="posts"/>
</template>

<script>
import PostList from '../components/PostList.vue'
import { ref } from 'vue'
import axios from 'axios'

export default {
    name: 'Home',
    components: { PostList },
    setup() {
        const posts = ref([])
        const error = ref(null)

        const loadPosts = async () => {
            try {
                // { params: { amount: 25 } }
                const response = await axios.get('http://127.0.0.1:8000/blog/featured/')

                if (!(response.status === 200)) { throw Error("Unable to load data")}

                console.log(response.data)
                posts.value = response.data
            }
            catch(err) {
                error.value = err.message
            }
        }
        
        if (!posts.value.length) { loadPosts() }

        return { posts, loadPosts }
    },
}
</script>

<style>

</style>

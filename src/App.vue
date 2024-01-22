<script>
import PostList from './components/PostList.vue'
import PostForm from './components/PostForm.vue'
import Chart from './components/Chart.vue'
export default {
  components:
      {
        PostList,PostForm, Chart
      },
  data() {
    return {
      posts:[
        {id:1,title:"js1",body:"gfgfgfgg"},
        {id:2,title:"js2",body:"gfgfgfgg"},
        {id:3,title:"js3",body:"gfgfgfgg"},
      ],

    }
  },
  methods: {
    createPost(post)
    {
      this.posts.push(post)
    }
  }

}
</script>

<template>
  <div class="app">
    <post-form
      @create ="createPost"
    />
    <post-list
        v-bind:posts="posts"
    />
    <chart/>


  </div>
</template>

<style>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

</style>
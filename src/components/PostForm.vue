<script>
export default
{
  data()
  {
    return {
      post:
          {
            title: '',
            body:''
          }
    }
  },
  methods:
      {
        createPost(event)
        {
          this.post.id=Date.now();
          this.$emit('create',this.post);
          this.post=
          {
            title: '',
            body:''
          }
        }
      }
}
</script>

<template>
  <form @submit.prevent>
    <h4>Создание поста</h4>
    <input
        v-model = "post.title"
           class="input"
           type="text"
           placeholder="Название">
    <input
        v-model="post.body"
           class="input"
           type="text"
           placeholder="Описание">
    <button @click="createPost" class="btn">Добавить</button>
  </form>
</template>

<style scoped>

</style>
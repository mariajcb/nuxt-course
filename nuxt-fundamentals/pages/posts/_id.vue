<template>
  <div class="container">
    <article>
      <h1 class="title">{{ post.title }}</h1>
      <p>{{ post.content }}</p>
    </article>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        id: this.$route.params.id,
        posts: [
          {
            id: 'couch',
            title: 'I will ruin the couch with my claws',
            content: 'jump on human and sleep on her all night long be long in the bed, purr in the morning and then give a bite to every human around for not waking up request food, purr loud scratch the walls, the floor, the windows, the humans hide head under blanket so no one can see'
          },
          {
            id: 'couch2',
            title: 'eat half my food and ask for more',
            content: 'jump on human and sleep on her all night long be long in the bed, purr in the morning and then give a bite to every human around for not waking up request food, purr loud scratch the walls, the floor, the windows, the humans hide head under blanket so no one can see'
          },
          {
            id: 'couch3',
            title: 'intently stare at the same spot',
            content: 'jump on human and sleep on her all night long be long in the bed, purr in the morning and then give a bite to every human around for not waking up request food, purr loud scratch the walls, the floor, the windows, the humans hide head under blanket so no one can see'
          }
        ]
      }
    },
    computed: {
      post () {
        return this.posts.find(post => post.id === this.id)
      }
    }
  }
</script>

<style scoped>
  .container {
    display: flex;
    justify-content: space-between;
    line-height: 1.5;
  }
  article * {
    margin-bottom: 1rem;
  }
  aside {
    min-width: 280px;
    max-width: 280px;
    padding-left: 2rem;
  }
  .title {
    font-size: 2rem;
  }
</style>

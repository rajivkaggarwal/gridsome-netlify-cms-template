<template>
  <Layout>
    <h1>Posts</h1>
    <div v-for="edge in $page.posts.edges" :key="edge.node.id">
      {{ edge.node.date }}
      {{ edge.node.title }}
      {{ edge.node.excerpt }}
    </div>

    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Error doloremque omnis animi, eligendi magni a voluptatum, vitae, consequuntur rerum illum odit fugit assumenda rem dolores inventore iste reprehenderit maxime! Iusto.</p>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Posts'
  }
}
</script>

<page-query>
query Post {
  posts: allPost {
    edges {
      node { 
        id
        title
        excerpt
        date (format: "MM/DD/YYYY H:mm:ss")
      }
    }
  }
}
</page-query>
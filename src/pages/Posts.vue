<template>
  <Layout>
    <h1>Posts</h1>
    <div v-for="edge in $page.posts.edges" :key="edge.node.id">
      <g-link :to="edge.node.path" class="post">
        <h2>{{ edge.node.title }}</h2>
    </g-link>
      {{ edge.node.date }}
      {{ edge.node.excerpt }}
    </div>
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
        path
      }
    }
  }
}
</page-query>
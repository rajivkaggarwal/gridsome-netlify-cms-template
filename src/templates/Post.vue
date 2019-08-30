<template>
  <Layout>
    <div class="journal">
      <div class="container journal-container">

        <div class="journal-header">
          <h1 v-html="$page.post.title" />
          <div class="date-container">
            <div class="date-label">Date:</div>
            <div v-text="$page.post.date"/>
          </div>
        </div>

        <div v-html="$page.post.content" />
      </div>
    </div>
  </Layout>
</template>

<page-query>
query Post ($path: String!) {
  post: post (path: $path) {
    title
    date (format: "D. MMMM YYYY")
    content
  }
}
</page-query>

<script>
export default {
  components: {
  },
  metaInfo () {
    return {
      title: this.$page.post.title
    }
  }
}
</script>

<style scoped>
.date-container {
  display: flex;
  flex-direction: row;
  align-items: baseline;
}
.date-label {
    font-size: 1.15rem;
    padding-right: 4px;
}

</style>

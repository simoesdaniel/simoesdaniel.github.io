<template>
  <ul>
    <li v-for="post in posts" :key="post.id">
      <div>{{ post.title }}</div>
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      posts: []
    };
  },
  methods: {
    loadPosts() {
      this.$axios
        .$get(
          "https://nuxt-course-ed535-default-rtdb.firebaseio.com/posts.json"
        )
        .then(res => {
          for (const key in res) {
            this.posts.push(res[key]);
          }
        });
    }
  },
  created() {
    this.loadPosts();
    console.log(this.posts);
  }
};
</script>

<style></style>

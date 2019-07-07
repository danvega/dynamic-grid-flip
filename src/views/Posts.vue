<template>
  <div id="app">
    <div class="posts">
      <div class="post" v-for="(post,index) in posts" :key="index">
        <img :src="require(`@/assets/img/${post.img}`)" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "posts",
  components: {},
  data() {
    return {
      posts: [
        { img: "codesandbox-custom-theme-cover.png" },
        { img: "escape-backtick-markdown-cover.png" },
        { img: "gridsome-codesandbox-plugin-cover.png" },
        { img: "live-coders-cover.png" },
        { img: "run-vue-visual-studio-code-cover.png" },
        { img: "triggering-events-router-vue-cover.png" },
        { img: "up-and-running-with-vue-cover.png" },
        { img: "vue-cli-validation-error.png" },
        { img: "vuepress-cookies-cover.png" }
      ]
    };
  }
};
</script>

<style scoped>
body {
  margin: 20px;
  padding: 0;
}
#app {
  width: 1000px;
  height: 80vh;
}
.posts {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 10px;
}
.post {
}
.post:first-child {
  grid-column: 1/3;
  grid-row: 1/3;
}
.post:nth-child(2),
.post:nth-child(3) {
  grid-column: 3;
}

.post:nth-child(4),
.post:nth-child(5) {
  grid-column: 1;
}
.post:nth-child(6) {
  grid-column: 2/4;
  grid-row: 3/5;
}

.post:nth-child(7) {
  grid-column: 1/3;
  grid-row: 5/7;
}

.post:nth-child(3),
.post:nth-child(5),
.post:nth-child(9) {
  display: flex;
  align-self: flex-end;
}

.post img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>

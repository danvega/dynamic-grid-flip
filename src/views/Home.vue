<template>
  <div id="home">
    <div class="posts">
      <div v-for="(post,index) in posts" :key="index" class="post" :class="getClass(index)">
        <img :src="require(`@/assets/img/${post.img}`)" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "home",
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
  },
  methods: {
    getClass(index) {
      if (index === 0) {
        return "foo";
      }
    }
  }
};
</script>

<style scoped>
#home {
  width: 1000px;
  height: 80vh;
}
.posts {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 10px;
}

.post:nth-child(1),
.post:nth-child(6),
.post:nth-child(7) {
  grid-column: span 2;
  grid-row: span 2;
}
.post:nth-child(6) {
  grid-column: 2/4;
  grid-row: 3/5;
}
.post:nth-child(4),
.post:nth-child(5) {
  grid-column: 1;
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

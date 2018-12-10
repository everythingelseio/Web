<template>
  <div id="app">
    <!-- <HeaderNav/> dont know how you want this to look yet, did some basic work, on flexing the content-->
    <PostFeed :FeedData="feed"/>
  </div>
</template>

<script>
// import HeaderNav from "./components/HeaderNav.vue";
import PostFeed from "./components/PostFeed.vue";

export default {
  name: "app",
  components: {
    // HeaderNav,
    PostFeed
  }
};
</script>

<style lang="scss">
html,
body {
  margin: 0;
  padding: 0;
}
</style>

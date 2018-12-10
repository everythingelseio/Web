<template>
  <main id="PostFeed">
    <div class="PostItem" v-for="item in FeedData" :key="item.postId">
      <div class="post image">
        <div class="PostInfo">
          <div class="PostName">NameOfBlog</div>
          <div class="PostControls">
            <i class="fas fa-retweet fa-2x"></i>
            <i class="far fa-heart fa-2x"></i>
          </div>
        </div>
        <div class="ImageContainer">
          <img src="img/image_0.gif">
        </div>
        <div class="ImageCaption">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut in molestie ligula. Suspendisse et
          neque sem. Nulla lorem tortor, finibus non lacinia ac, suscipit sit amet elit.
        </div>
      </div>
    </div>
  </main>
</template>


<script>
export default {
  name: "PostFeed",
  props: {
    FeedData: Array
  }
};
</script>

<style scoped lang="scss">
.post {
  background-color: white;
  width: 100%;
  height: auto;
  border-radius: 30px;
  position: relative;
  margin-bottom: 10px;
  -webkit-box-shadow: 10px 10px 28px -10px rgba(0, 0, 0, 0.75);
  -moz-box-shadow: 10px 10px 28px -10px rgba(0, 0, 0, 0.75);
  box-shadow: 10px 10px 28px -10px rgba(0, 0, 0, 0.75);

  .PostInfo {
    height: 30px;
    width: auto;
    position: absolute;
    padding-left: 15px;
    padding-right: 10px;
    padding-top: 10px;
    z-index: 2;
    background-color: rgba(0, 0, 0, 0.3);
    border-bottom-right-radius: 10px;
    color: #fff;

    .BlogInfo {
      visibility: hidden;
      position: absolute;
      z-index: 5;
      position: relative;
      left: -100px;
      img {
        width: 60px;
        height: auto;
        border-radius: 50%;
      }
    }
    &:hover .BlogInfo {
      visibility: visible;
    }
  }

  .PostControls {
    position: absolute;
    right: 0;
    margin-right: 20px;
    margin-top: 10px;
    z-index: 2;
    i {
      color: #fff;
      font-weight: 900;
      width: 40px;
      height: 40px;

      &:hover {
        color: red;
      }
    }
  }

  img {
    width: 100%;
    transform: translateX(-50%);
    margin-left: 50%;
    border-radius: 30px 30px 0 0;
  }

  .ImageContainer {
    padding-bottom: 5px;
    margin-bottom: 5px;
  }

  .ImageCaption {
    height: 40px;
    padding: 10px;
  }
}
</style>

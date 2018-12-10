<template>
  <header>
    <img src="../assets/logo.png">
    <div id="Navigation">
      <div class="NavItem">
        <button class="NavButton">Home</button>
      </div>
      <div class="NavItem">
        <button class="NavButton">Trending</button>
      </div>
      <div class="NavItem">
        <button class="NavButton">MeMes</button>
      </div>
      <div class="NavItem">
        <button class="NavButton">About</button>
      </div>
    </div>
  </header>
</template>


<script>
export default {
  name: "HeaderNav",
  props: {
    msg: String
  }
};
</script>

<style scoped lang="scss">
header {
  width: 100%;
  position: fixed;
  top: 0;
  height: 40px;
  background: red; //   for debug
  display: flex;
  justify-content: space-between;

  img {
    max-width: 40px;
    height: auto;
  }

  #Navigation {
    width: 500px;
    display: flex;
    justify-content: space-around;

    .NavItem {
      display: inline-block;
      color: black;
      .NavButton {
        height: 40px;
        width: 40px;
      }
    }
  }
}
</style>

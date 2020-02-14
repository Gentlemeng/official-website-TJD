<template>
  <div id="header">
    <section id="header-content">
      <h1 id="logo">
        <img />
      </h1>
      <div id="header-nav">
        <customNav />
      </div>
      <button id="login-btn">
        <a href="http://data.tjresearch.cn" target="_blank">登录</a>
      </button>
    </section>
    <section id="banner">
         
    </section>
  </div>
</template>

<script>

import customNav from "./nav";
export default {
  data() {
    return {};
  },
  components: {
    customNav
  },
  methods: {
    // handleLogin(){
    //     window.location.href = 'http://data.tjresearch.cn'
    // }
  }
};
</script>

<style lang="scss" scoped>
#header-content {
  display: flex;
  align-items: center;
  height: 100px;
  font-size: 18px;
  background-color: #ffffff;
  h1 {
    display: flex;
    width: 640px;
    height: 100px;
    max-width: 640px;
    padding: 0 200px;
    img {
      flex: 1;
      background-color: lightblue;
    }
  }
  #header-nav {
    flex: 1;
    display: flex;
    justify-content: flex-end;
  }
}
#login-btn {
  border: none;
  font-size:18px;
  a {
    display: inline-flex;
    align-items: center;
    height: 40px;
    padding: 0 50px;
    color: #fff;
    border: 1px solid #ff8252;
    border-radius: 20px;
    background-color: #ff8252;
    cursor: pointer;
  }
  margin-right: 34px;
}
#banner {
  height: 600px;
  background-color: #ff854c;
}
</style>
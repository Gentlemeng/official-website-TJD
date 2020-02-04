<template>
  <!-- <div id="nav"> -->
  <ul id="nav-ul">
    <li
      v-for=" (data,index) in navData"
      :key="data.title"
      :class="activeIndex==index?'active nav-li':'nav-li'"
    >
      <router-link :to="data.path" target="_self">
        <button :class="data.disabled?'disabled':''" :disabled="data.disabled">{{data.title}}</button>
      </router-link>
    </li>
  </ul>
  <!-- </div> -->
</template>

<script>
export default {
  data() {
    return {
      navData: [
        {
          title: "首页",
          path: "home",
          disabled: false
        },
        {
          title: "产品中心",
          path: "product",
          disabled: false
        },
        {
          title: "指标说明",
          path: "indexInfo",
          disabled: false
        },
        {
          title: "关于我们",
          path: "aboutUs",
          disabled: false
        }
      ],
      activeIndex: 0
    };
  },
  watch: {
    $route(to, from) {
      let path = to.path.split("/")[1];
      let index = this.navData.findIndex(data => path == data.path);
      this.activeIndex = index;
    }
  },
  methods: {}
};
</script>

<style lang="scss" scoped>
#nav-ul {
  display: flex;
}
// header nav 样式
#header-nav {
  .nav-li {
    text-align: center;
    line-height: 100px;
    margin-right: 50px;
  }
  .nav-li a {
    display: inline-block;
    padding: 0 50px 0;
    line-height: 40px;
    cursor: pointer;
    button {
      font-size: 18px;
      color: #000;
      border: none;
      background: none;
      padding: 0;
      cursor: pointer;
    }
  }
  .nav-li.active a {
    border: 1px solid #ff8252;
    border-radius: 20px;
  }
  .nav-li.active button {
    color: #ff8252;
  }
}

// footer nav 样式
#footer-nav-content {
  .nav-li {
    text-align: center;
    line-height: 70px;
    margin-right: 20px;
  }
  .nav-li a {
    display: inline-block;
    margin: 0 20px 0;
    height: 70px;
    line-height: 70px;
    cursor: pointer;
    button {
      font-size:18px;
      color: #fff;
      border: none;
      background: none;
      padding: 0;
      cursor: pointer;
    }
  }
  .nav-li.active a {
    border-bottom:3px solid #fff;
  }
  .nav-li.active button {
  }
}
</style>
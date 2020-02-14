<template>
  <div id="home">
    <section id="home-product">
      <h3 class="module-title">产品中心</h3>
      <ul class="product-ul">
        <li class="product-list" v-for="(data,index) in productList" :key="index">
          <div class="product-list-icon"></div>
          <h5 class="product-list-title">{{data.title}}</h5>
          <p class="product-list-desc">{{data.desc}}</p>
          <div class="product-list-bottom">
            <div class="product-list-time">
              <p class="list-month">{{data.day}}/{{data.month}}</p>
              <p class="list-year">{{data.year}}</p>
            </div>
            <router-link to="product" target="_blank">
              <button class="product-list-btn">立即查看</button>
            </router-link>
          </div>
        </li>
      </ul>
    </section>
    <section id="home-index">
      <h3 class="module-title">指标说明</h3>
      <div class="home-index-box">
        <div class="index-bg"></div>
        <div class="index-info">
          <p class="index-info-cn">数据就是数值，也就是我们通过观察实验或计算得出的结果。</p>
          <p
            class="index-info-en"
          >nspection Operating Platform of Big Data Science and Technology CenterMultilex Data Operation Recovery</p>
          <router-link to="indexInfo" target="_blank">
            <button class="index-btn">查看详情</button>
          </router-link>
        </div>
      </div>
    </section>
    <section id="home-about">
      <h3 class="module-title">关于我们</h3>
      <ul class="home-about-ul">
        <li class="home-about-li" v-for="(data,index) in aboutArr" :key="index">
          <div class="home-about-icon">icon</div>
          <h5 class="home-about-title">{{data.title}}</h5>
          <p class="home-about-database">{{data.database}}</p>
          <p class="home-about-desc">{{data.desc}}</p>
        </li>
      </ul>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      productList: [
        {
          title: "宏观",
          desc: "我来打酱油",
          day: "23",
          month: "03",
          year: "2020"
        },
        {
          title: "行业",
          desc: "我来打酱油",
          day: "23",
          month: "03",
          year: "2020"
        },
        {
          title: "拉动",
          desc: "我来打酱油",
          day: "23",
          month: "03",
          year: "2020"
        },
        {
          title: "关联",
          desc: "我来打酱油",
          day: "23",
          month: "03",
          year: "2020"
        },
        {
          title: "结构",
          desc: "我来打酱油",
          day: "23",
          month: "03",
          year: "2020"
        }
      ],
      aboutArr: [
        {
          title: "标题",
          database: "database",
          desc: "数据就是数值，也就是我们通过观察实验或计算得出的结果。"
        },
        {
          title: "标题",
          database: "database",
          desc: "数据就是数值，也就是我们通过观察实验或计算得出的结果。"
        },
        {
          title: "标题",
          database: "database",
          desc: "数据就是数值，也就是我们通过观察实验或计算得出的结果。"
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
#home-about {
  height: 644px;
  padding: 140px 312px 0;
  .home-about-ul {
    margin-top: 70px;
    display: flex;
    justify-content: space-around;
    .home-about-li {
      width: 390px;
      padding: 50px 90px;
      text-align: center;
      &:hover {
        .home-about-icon {
          color: #ff845c;
        }
        box-shadow: 0px 5px 10px rgba(0, 0, 0, 0.3);
      }
    }
    .home-about-icon {
      height: 90px;
      margin-bottom: 18px;
      font-size: 38px;
    }
    .home-about-title {
      line-height: 30px;
      font-size: 22px;
      color: #04121f;
    }
    .home-about-database {
      line-height: 22px;
      font-size: 18px;
      color: #595a5c;
    }
    .home-about-desc {
      line-height: 24px;
      font-size: 14px;
      color: #6f6f6f;
    }
  }
}
#home-index {
  height: 818px;
  padding: 90px 340px 0;
  background-color: #fafafc;
  .home-index-box {
    display: flex;
  }
  .index-bg {
    width: 710px;
    height: 430px;
    margin: 107px 0 0;
  }
  .index-info {
    // display:flex;
    flex: 1;
    flex-direction: column;
    justify-content: center;
    padding-left: 45px;
    color: #04121f;
    text-align: center;
    .index-info-cn {
      line-height: 44px;
      font-size: 38px;
      margin-top: 97px;
      margin-bottom: 45px;
      text-align: left;
    }
    .index-info-en {
      line-height: 44px;
      font-size: 20px;
      margin-bottom: 60px;
      text-align: left;
    }
    .index-btn {
      line-height: 40px;
      padding: 0 40px;
      font-size: 18px;
      color: #fff;
      background-color: #ff854c;
      border-radius: 20px;
    }
  }
}
#home-product {
  padding: 68px 312px 0;
  overflow: hidden;
  .product-ul {
    display: flex;
    margin: 57px auto 40px;
    justify-content: space-between;
    .product-list {
      width: 250px;
      margin: 0 5px 0;
      padding: 14px;
      color: #000;
      background-color: #fff;
      box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.3);
      .product-list-icon {
        width: 90px;
        height: 90px;
        margin: 80px auto 86px;
        background-color: #ff854c;
      }
      .product-list-title {
        line-height: 40px;
        font-size: 18px;
      }
      .product-list-desc {
        line-height: 16px;
        margin-bottom: 10px;
        font-size: 14px;
      }
      .product-list-bottom {
        display: flex;
        justify-content: space-between;
        align-items: center;
        .product-list-time {
          color: #555;
          .list-month {
            line-height: 30px;
            font-size: 20px;
          }
          .list-year {
            line-height: 16px;
            font-size: 14px;
          }
        }
        .product-list-btn {
          padding: 0 16px;
          line-height: 28px;
          text-align: center;
          font-size: 14px;
          color: #fff;
          background-color: #ff854c;
          border-radius: 14px;
        }
      }
    }
  }
}
</style>

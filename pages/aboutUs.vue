<template>
  <div id="about-us">
    <section id="who-am-i">
      <h3 class="module-title">我们是谁</h3>
      <h4
        class="who-am-i-con"
      >“数字时代的经济活动实时在线分析预测系统”（以下简称“本系统”）是腾景产业研究院开展的一项长期研究项目。腾景产业研究院是适应互联网和数字时代特点和要求，旨在推动宏观和产业经济研究方法变革、推动实体经济领域产业互联网发展的新型智库机构。</h4>
    </section>
    <section id="method">
      <div class="method-box">
        <h4 class="method-title">这是一个前所未有的预测方法</h4>
        <h5 class="method-con">
          本系统以GFP为出发点和主线构造而成，
          <br />而GFP是在对现有统计体系中的GDP重要变革基础上形成的。
          <br />创造性利用投入产出架构和高频数据
        </h5>
      </div>
    </section>
    <section id="unique">
      <section id="unique-content">
        <h3 class="module-title">为什么与众不同</h3>
        <ul id="unique-con-ul">
          <li class="unique-list" v-for="(data,index) in uniqueList" :key="index">
            <div class="unique-list-icon"></div>
            <div class="unique-list-con">
              <p class="unique-list-title">{{data.title}}</p>
              <p class="unique-list-text">{{data.text}}</p>
            </div>
          </li>
        </ul>
      </section>
      <section id="unique-icon">
        <div class="unique-icon-bg">
          <ul class="unique-icon-ul">
            <li class="unique-icon-li" v-for="(data,index) in advantageIconArr"
                :key="index">
              <div class="advantage-icon"></div>
              <p class="advantage-text">{{data.text}}</p>
            </li>
          </ul>
        </div>
      </section>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      uniqueList: [
        {
          icon: "",
          title: "创造性地运用投入产业框架",
          text: "把静态分析体系转化为能够反映高度复杂关联关系的实时跟踪系统"
        },
        {
          icon: "",
          title: "创造性地运用投入产业框架",
          text: "把静态分析体系转化为能够反映高度复杂关联关系的实时跟踪系统"
        },
        {
          icon: "",
          title: "创造性地运用投入产业框架",
          text: "把静态分析体系转化为能够反映高度复杂关联关系的实时跟踪系统"
        },
        {
          icon: "",
          title: "创造性地运用投入产业框架",
          text: "把静态分析体系转化为能够反映高度复杂关联关系的实时跟踪系统"
        },
        {
          icon: "",
          title: "创造性地运用投入产业框架",
          text: "把静态分析体系转化为能够反映高度复杂关联关系的实时跟踪系统"
        },
        {
          icon: "",
          title: "创造性地运用投入产业框架",
          text: "把静态分析体系转化为能够反映高度复杂关联关系的实时跟踪系统"
        }
      ],
      advantageIconArr:[
          {
              iconUrl:'',
              text:"优势"
          },
          {
              iconUrl:'',
              text:"优势"
          },{
              iconUrl:'',
              text:"优势"
          },{
              iconUrl:'',
              text:"优势"
          },{
              iconUrl:'',
              text:"优势"
          },
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
#who-am-i {
  height: 577px;
  margin: 0 400px;
  overflow: hidden;
  .module-title {
    margin-top: 100px;
  }
  .who-am-i-con {
    line-height: 30px;
    margin: 60px 220px 0;
    font-size: 16px;
  }
}
#method {
  // overflow: hidden;
  position: relative;
  height: 600px;
  background-color: #292d30;
  .method-box {
    overflow: hidden;
    position: absolute;
    left: 350px;
    bottom: 0;
    width: 630px;
    // margin-top:3.3px;
    // margin-left:3.5px;
    background-color: #fff;
    text-align:center;
    .method-title {
      margin: 50px auto 20px;
      height: 60px;
      line-height: 60px;
      font-size: 36px;
    }
    .method-con {
      margin: 0 70px 50px;
      line-height: 30px;
      font-size: 16px;
    }
  }
}
#unique {
  // height:9.5px;
  #unique-content {
    // display:flex;
    margin: 100px 400px 0;
    #unique-con-ul {
      display: flex;
      max-width: 100%;
      flex-wrap: wrap;
      margin-top: 38px;
      margin-bottom: 60px;
      .unique-list {
        display: flex;
        width: 50%;
        // min-width:50%;
        flex: 1;
        margin-bottom: 26px;
        .unique-list-icon {
          width: 50px;
          height: 50px;
          margin: 8px 56px 0 8px;
          background-color: bisque;
        }
        .unique-list-con {
          max-width: 284px;
          width: 284px;
          text-align: left;
          .unique-list-title {
            height: 30px;
            line-height: 30px;
            font-size: 18px;
            font-weight: bold;
          }
          .unique-list-text {
            font-size: 14px;
            line-height: 26px;
            color: #4a4a4a;
          }
        }
      }
      .unique-list:nth-child(2n + 1) {
        min-width: 50%;
        margin-right: 50px;
      }
    }
  }
  #unique-icon {
    .unique-icon-bg {
        padding-left:450px;
        background-color:rgba(0,0,0,.5);
        overflow: hidden;
      .unique-icon-ul {
          display:flex;
            margin: 55px auto 45px;
        .unique-icon-li {
          .advantage-icon {
            width: 120px;
            height: 120px;
            margin: 30px 40px 10px;
            background-color: #fe864a;
          }
          .advantage-text {
              height:50px;
              line-height:50px;
              color:#fff;
              text-align:center;
              font-size:18px;
          }
        }
      }
    }
  }
}
</style>
<template>
  <div id="footer">
    <section id="subscribe">
      <h3 class="module-title">产品订阅</h3>
      <section class="company-contact">
        <div class="company-contact-list" v-for="(data,index) in companyContactArrs"
          :key="index">
          <div class="company-contact-icon"></div>
          <div class="company-contact-text">{{data.text}}</div>
        </div>
      </section>
      <section class="user-info">
        <form action="http://localhost:3000">
          <div class="form-col">
            <input class="form-input" type="text" name="name" placeholder="姓名：">
            <input class="form-input" type="text" name="tel" placeholder="电话：">
          </div>
          <div class="form-col">
            <input class="form-input" type="text" name="email" placeholder="邮箱：">
            <input class="form-input" type="text" name="pxarks" placeholder="信息备注：">
          </div>
          <input class="submit-btn" type="submit" value="提交信息">
        </form>
      </section>
    </section>
    <section id="footer-info">
      <div id="footer-info-top">
        <div id="footer-nav">
          <h2 id="footer-logo">
            <img />
          </h2>
          <div id="footer-nav-content">
              <customNav/>
          </div>
        </div>
        <div id="footer-tel">
            <p>TEL:{{tel}}</p>
            <p>核心优势  加入我们</p>
        </div>
      </div>
      <div id="footer-info-bottom">
          <div id="footer-links">
              友情链接：
              <ul>
                  <li v-for="(data,index) in links" :key="index">
                      <a :href="data.link" target="_blank">{{data.name}}</a>
                  </li>
              </ul>
          </div>
          <div id="copy-right">
              {{copyRight}}&nbsp;&nbsp;&nbsp;&nbsp;
              <a id="beian" href="http://www.beian.miit.gov.cn">备案号：*********</a>
          </div>
      </div>
    </section>
  </div>
</template>

<script>
import customNav from "./nav";
export default {
  components: {
    customNav
  },
  data() {
      return {
        companyContactArrs:[
            {
              icon:'',
              text:'公司地址',
            },
            {
              icon:'',
              text:'公司电话',
            },{
              icon:'',
              text:'公司邮箱',
            },
          ],
          tel: "400-222-333",
          links:[
              {
                  name:"网站名称",
                  link:"http://www.baidu.com"
              },
              {
                  name:"网站名称",
                  link:"http://www.baidu.com"
              },
              {
                  name:"网站名称",
                  link:"http://www.baidu.com"
              },
          ],
          copyRight:"版权声明©腾景研究院2019-2020"
      }
  },
};
</script>

<style lang="scss" scoped>
 
#footer {
  overflow: hidden;
}
#subscribe {
  height: 770px;
  padding: 100px 390px 0;
  overflow: hidden;
  /* background-color:#ff854c; */
}
.company-contact{
  display:flex;
  margin:76px auto 80px;
  .company-contact-list{
    flex:1;
    .company-contact-icon{
      width:60px;
      height:60px;
      background-color: #262d33;
      margin:0 auto 23px;
    }
    .company-contact-text{
      height:40px;
      line-height: 40px;
      text-align: center;
      font-size:18px;
      color:#6f6f6f;
    }
  }
}
.user-info{
  margin-bottom:116px;
  form{
    display:flex;
    align-items: center;
    .form-col{
      display:flex;
      flex-direction: column;
      margin-right:50px;
      .form-input{
        width:400px;
        height:68px;
        line-height:68px;
        margin:20px 0;
        font-size:18px;
        color:#b8b8b8;
        border:2px solid #b5b5b5;
        border-radius:6px;
        text-indent:12px;
      }
    }
    .submit-btn{
      width:100%;
      height:58px;
      line-height:58px;
      text-align: center;
      font-size:20px;
      color:#fff;
      background-color: #ff854c;
      border-radius:6px;
      box-shadow: 1px 1px 4px rgba(0,0,0,.8);
    }
    ::-webkit-input-placeholder{
      color:#b8b8b8;
    }
    ::-moz-placeholder{
      color:#b8b8b8;
    }
    :-ms-input-placeholder{
      color:#b8b8b8;
    }
  }
}
#footer-info {
  /* height: 2.23px; */
  padding: 40px 0;
  background-color: #262d33;
  #footer-info-top {
      box-sizing: content-box;
    display: flex;
    justify-content: space-between;
    // height: 0.7px;
    padding: 0 362px 0 370px;
    border-bottom: 2px solid #000000;
    #footer-nav {
        display: flex;
    //   margin-left: 0.16px;
      h2#footer-logo {
        height: 70px;
        padding: 15px 40px 0 0;
        img {
          display: inline-block;
          width: 100px;
          height: 40px;
        }
      }
    }
    #footer-tel {
        display: flex;
        flex-direction: column;
      height: 70px;
      padding:10px 0;
    //   margin-right: 0.5px;
      font-size:18px;
      color:#fff;
      p{
          text-align: right;
      }
    }
  }
  #footer-info-bottom {
      display:flex;
      justify-content: space-between;
      height:40px;
      margin:30px 362px 0 370px;
      #footer-links{
          display:flex;
          line-height: 40px;
          color:#fff;
          ul{
              display:flex;
              
              li{
                //   line-height: .4px;
                margin-right:18px;
                  a{
                      color:#fff;
                  }
              }
          }
      }
      #copy-right{
          line-height:40px;
          color:#fff;
          #beian{
              color:#fff;
          }
      }
  }
}
</style>
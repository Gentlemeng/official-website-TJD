<template>
  <div id="footer">
    <section id="subscribe">产品订阅</section>
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
  padding: 100px 312px 0;
  /* background-color:#ff854c; */
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
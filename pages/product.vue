<template>
    <div id="product">
        <section id="product-content">
            <!-- <section id="product-title"></section> -->
            <!-- <section id="product-list-head"></section> -->
            <h3 class="product-list-title">产品列表</h3>
            <section id="product-list-tab">
                <ul class="product-tab-top">
                    <li :class="activeIndex==index?'active product-tab-li':'product-tab-li'"
                        v-for="(text,index) in productTabBtns"
                        :key="index" @click="handleSwitchTabs(index)">
                        {{text}}
                    </li>
                </ul>
                <div class="product-tab-bottom">
                    <div class="tab-btn product-pre-btn">
                        <span @click="handlePre()">上</span>
                    </div>
                    <div class="tab-btn product-next-btn">
                        <span @click="handleNext()">下</span>
                    </div>
                    <ul class="product-tab-con">
                        <li class="product-tab-con-list"
                            v-for="(data,index) in productTabCons"
                            :key="index"
                            v-show="index==activeIndex">{{data.text}}
                        </li>
                    </ul>
                </div>
            </section>
            <ul id="product-ul">
                <li 
                    v-for="(data) in productInfoArr" :key="data.name"
                    class="product-li">
                    <div class="product-info-bg"></div>
                    <div class="product-info-decs">
                        <h4 class="product-decs-top">
                            <p class="product-decs-name">{{data.name}}</p>&nbsp;&nbsp;
                            <a href="#subscribe" class="product-info-decs-btn">订阅&gt;&gt;</a>
                        </h4>
                        <p class="product-decs-bottom">
                            {{data.describe}}
                        </p>
                    </div>
                </li>
            </ul>
        </section>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                activeIndex:0,
                productTabBtns: [
                    "宏观",
                    "行业",
                    "拉动",
                    "关联",
                    "结构",
                ],
                productTabCons:[
                    {
                        imgUrl:"",
                        text:"1"
                    },
                    {
                        imgUrl:"",
                        text:"2"
                    },
                    {
                        imgUrl:"",
                        text:"3"
                    },
                    {
                        imgUrl:"",
                        text:"4"
                    },
                    {
                        imgUrl:"",
                        text:"5"
                    },
                ],
                productInfoArr:[
                    {
                        name:"宏观",
                        describe:"我是来打酱油的...",
                    },{
                        name:"行业",
                        describe:"我是来打酱油的...",
                    },{
                        name:"拉动",
                        describe:"我是来打酱油的...",
                    },{
                        name:"关联",
                        describe:"我是来打酱油的...",
                    },{
                        name:"结构",
                        describe:"我是来打酱油的...",
                    },
                ]
            }
        },
        methods:{
            handleSwitchTabs(index){
                this.activeIndex = index;
            },
            handlePre(){
                // debugger
                if(this.activeIndex===0){
                    
                    this.activeIndex = this.productTabCons.length-1
                } else{
                    this.activeIndex--
                }
            },
            handleNext(){
                
                if(this.activeIndex===this.productTabCons.length-1){
                    this.activeIndex = 0
                } else{
                    this.activeIndex++
                }
            }
        }
    }
</script>

<style lang="scss" scoped>
    .product-list-title{
    height:110px;
    line-height:110px;
    padding:0 300px;
    font-size:36px;
    background-color: #fafafa;
    text-indent: 40px;
    text-align: left;
}
#product-list-tab{
    // height:620px;
    .product-tab-top{
        display:flex;
        padding:14px 300px 0;
        margin-bottom:40px;
        background-color: #fafafa;
        .product-tab-li{
            line-height:66px;
            padding:0 28px;
            font-size:18px;
            cursor:pointer;
        }
        .product-tab-li:first-child{
            margin-left:40px;
        }
        .product-tab-li.active{
            color:#fe884b;
            border-bottom:2px solid #fe884b;
        }
    }
    .product-tab-bottom{
        margin:0 300px 50px;
        height:520px;
        // display:flex;
        position: relative;;
        .tab-btn{
            // display:none;
            // visibility: hidden;
            position:absolute;
            width:220px;
            height:100%;
            background-color:rgba(254,136,75,.0);
            z-index: 2;
            span{
                display:none;
                position:absolute;
                left:50%;
                top:50%;
                width:20px;
                height:40px;
                margin:-20px 0 0 -10px;
            }
        }
        .tab-btn:hover{
            // visibility: visible;
            background-color:rgba(254,136,75,.5);
            span{
                display:block;
            }
        }
        .product-pre-btn{
            left:0;
            top:0;
        }
        .product-next-btn{
            right:0;
            top:0;
        }
        .product-tab-con{
            width:100%;
            height:100%;
            position:relative;
            background-color:rgba(0,0,0,1);
            .product-tab-con-list{
                width:100%;
                height:100%;
                position:absolute;
                color:#fff;
                left:0;
                top:0;
            }
        }

    }
}
#product-ul{
    padding:100px 0;
}
#product-ul .product-li{
    display:flex;
    justify-content:space-between;
    padding:100px 300px;
    &:nth-child(2n+1){
        
        background-color:#fafafa;
    }
    &:nth-child(2n){
        flex-direction: row-reverse;
    }
    .product-info-bg{
        width:540px;
        height:300px;
        background-color:#000;
    }
    .product-info-decs{
        width:680px;
        overflow: hidden;
        .product-decs-top{
            display:flex;
            justify-content:center;
            align-items: center;
            font-size:30px;
            height:60px;
            margin:70px 0 22px;
            .product-decs-name{
                
            }
            .product-info-decs-btn{
                // margin-top:.3px;
                font-size:14px;
                color:#fe884b;
                cursor: pointer;
            }
        }
        .product-decs-bottom{
            padding:0 44px;
            line-height:24px;
            color:#838383;
            font-size:14px;
            text-align:left;
        }
    }
    
}
</style>
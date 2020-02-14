<template>
    <div id="index-info">
        <section id="index-introduce">
            <h3 class="index-intro-title">我们的指标</h3>
            <p class="index-intro-text">我是来打酱油的...</p>
            <div class="index-intro-bg">
                <div class="index-intro-pos">
                    <ul class="index-intro-ul">
                        <li class="index-intro-list"
                            v-for="(data,index) in indexIntroArr" :key="index">
                            <div class="index-intro-circle">
                                <span class="index-intro-icon"></span>
                                <div class="index-intro-circle-active">
                                    <p>
                                        <span>{{data.introduce+data.introduce+data.introduce+data.introduce}}</span>
                                    </p>
                                </div>
                            </div>
                            <p class="index-intro-list-text">{{data.text}}</p>
                        </li>
                    </ul>
                </div>
            </div>
        </section>
        <ul id="index-series">
            <li class="index-series-li"
                v-for="data in indexSeriesArr"
                :key="data.name">
                <div class="index-series-text">
                    <h3 class="index-series-name">{{data.name}}</h3>
                    <p class="index-series-desc">{{data.describe}}</p>
                </div>
                <div class="index-series-bg"></div>
            </li>
        </ul>
        <section id="index-feature">
            <div id="index-feature-box">
                <span class="pre-feature-btn">上</span>
                <span class="next-feature-btn">下</span>
                <ul class="feature-ul">
                    <li class="feature-list"
                        v-for="(data,index) in featureArr" :key="index">
                        <div class="feature-top">
                            <h4 class="feature-title">{{data.title}}</h4>
                            <p class="feature-text">{{data.text}}</p>
                            <div class="feature-bg">
                                <div class="feature-bg-active"></div>
                            </div>
                        </div>
                        <p class="feature-desc">{{data.desc}}</p>
                    </li>
                </ul>
            </div>
        </section>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                indexIntroArr: [
                    {
                        text:"腾景全口径",
                        icon:"",
                        introduce:"我是来打酱油的..."
                    },
                    {
                        text:"腾景全口径",
                        icon:"",
                        introduce:"我是来打酱油的..."
                    },{
                        text:"腾景全口径",
                        icon:"",
                        introduce:"我是来打酱油的..."
                    },
                    {
                        text:"腾景全口径",
                        icon:"",
                        introduce:"我是来打酱油的..."
                    }
                ],
                indexSeriesArr:[
                    {
                        name:"消费全口径数据",
                        describe:"我是来打酱油的...",
                    },{
                        name:"投资全口径数据",
                        describe:"我是来打酱油的...",
                    },{
                        name:"进出口全口径数据",
                        describe:"我是来打酱油的...",
                    }
                ],
                featureArr:[
                    {
                        title:"特点",
                        text:"Cardiology",
                        icon:"",
                        desc:"我又来打酱油来。。。"
                    },{
                        title:"特点",
                        text:"Cardiology",
                        icon:"",
                        desc:"我又来打酱油来。。。"
                    },{
                        title:"特点",
                        text:"Cardiology",
                        icon:"",
                        desc:"我又来打酱油来。。。"
                    },{
                        title:"特点",
                        text:"Cardiology",
                        icon:"",
                        desc:"我又来打酱油来。。。"
                    },{
                        title:"特点",
                        text:"Cardiology",
                        icon:"",
                        desc:"我又来打酱油来。。。"
                    },{
                        title:"特点",
                        text:"Cardiology",
                        icon:"",
                        desc:"我又来打酱油来。。。"
                    },
                    // {
                    //     title:"特点",
                    //     text:"Cardiology",
                    //     icon:"",
                    //     desc:"我又来打酱油来。。。"
                    // }
                ]
            }
        },
    }
</script>

<style lang="scss" scoped>
#index-info{
    overflow: hidden;
}
#index-introduce{
    text-align:center;
    .index-intro-title{
        margin:50px auto 26px;
        line-height:50px;
        font-size:28px;
    }
    .index-intro-text{
        margin:0 auto 160px;
        line-height:24px;
        color:#7c7c7c;
        font-size:14px;
    }
    .index-intro-bg{
        position: relative;
        height: 204px;
        padding:0 300px;
        background-color: #eeeeee;
        .index-intro-pos{
            position:absolute;
            left:300px;
            top:-50%;
        }
    }
    .index-intro-ul{
        display:flex;
        .index-intro-list{
            margin:0 50px;
            
        }
        .index-intro-circle{
            position:relative;
            width:210px;
            height:210px;
            margin-bottom:10px;
            border:1px solid #eeeeee;
            border-radius: 50%;
            background-color:#fff;
            box-shadow: 0px 0px 10px 2px #eee;
            &:hover .index-intro-circle-active{
                // z-index: 0;
                visibility: visible;
                box-shadow: 0px 0px 10px 2px #ff854c;
            }
            .index-intro-icon{

            }
            .index-intro-circle-active{
                visibility: hidden;
                position:absolute;
                top:0;
                left:0;
                width:210px;
                height:210px;
                border:1px solid #ff854c;
                border-radius: 50%;
                background-color: #ff854c;
                // z-index:-1;
                p{
                    width:100%;
                    height:100%;
                    display:flex;
                    justify-content: center;
                    align-items: center;
                    color:#fff;
                    span{
                        max-width:70%;
                        max-height:80%;
                        line-height:18px;
                    }
                }
            }
        }
        .index-intro-list-text{
            line-height: 50px;
            font-size:28px;
            color:#3a3a3a;
        }
    }
}
#index-series{
    margin: 70px 370px 0 350px;
    overflow: hidden;
}
.index-series-li{
    display:flex;
    height:446px;
    margin-bottom:180px;
    box-shadow: 4px 20px 20px #eee;
    &:nth-child(2n+1){
        flex-direction: row;
    }
    &:nth-child(2n){
        flex-direction: row-reverse;
    }
    .index-series-text{
        flex:1;
        text-align:left;
        .index-series-name{
            margin:74px 70px 0 70px;
            line-height:110px;
            font-size:48px;
        }
        .index-series-desc{
            margin:0 70px 0 70px;
            line-height:30px;
            color:#838383;
            font-size:18px;
        }
    }
    .index-series-bg{
        flex:1;
        background-color:#e7d6cf;
    }
}
#index-feature{
    // height:7.14px;
    overflow: hidden;
    background-color:#d9ac95;
}
#index-feature-box{
    margin:130px 50px 110px;
    
    position:relative;
    span{
        position:absolute;
        top:50%;
        width:50px;
        height:50px;
        margin-top:-25px;
        background-color:#fff;
        box-shadow: -8px 8px 10px rgba(0, 0, 0, 0.3);
    }
    .pre-feature-btn{
        left:-10px;
    }
    .next-feature-btn{
        right:-10px;
    }
}
.feature-ul{
    display:flex;
    .feature-list{
        margin:30px 15px 0;
        .feature-top{
            padding:14px 16px;
            margin-bottom:30px;
            background-color:#fff;
            .feature-title{
                line-height:60px;
                font-size:36px;
                color:#000;
            }
            .feature-text{
                margin-bottom:12px;
                line-height:44px;
                font-size:18px;
                color:#eceaff;
            }
            .feature-bg{
                width:240px;
                height:200px;
                background-color:#eceaff;
                .featrue-bg-active{

                }   
            }
        }
        .feature-desc{
            margin:0 12px;
            line-height:30px;
            font-size:16px;
            color:#fff;
        }
    }
}
</style>
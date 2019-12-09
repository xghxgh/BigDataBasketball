<template>
  <div class="left-chart">
    <div class="lc-header">排行榜</div>
    <div class="lc-list">
      <div class="lc-list-dongbu">
        <div class="list-dongbu-content">东部</div>
        <dv-scroll-ranking-board class="list-dongbu" :config="config1"/>
      </div>
<!--      <dv-scroll-ranking-board :config="config" style="width:500px;height:300px" />-->
      <div class="lc-list-xibu">
        <div class="list-xibu-content">西部</div>
        <dv-scroll-ranking-board class="list-xibu" :config="config2"/>
      </div>
    </div>

  </div>
</template>

<script>
    export default {
        name: "LeftChart",
        data(){
            return{
                config1:{
                    data:[
                        {
                            name:'雄鹿',
                            value:87
                        },{
                            name:'凯尔特人',
                            value:76.2
                        },{
                            name:'热火',
                            value:73.9
                        },{
                            name:'76人',
                            value:70.8
                        },{
                            name:'猛龙',
                            value:68.2
                        },{
                            name:'步行者',
                            value:65.2
                        },{
                            name:'篮网',
                            value:56.5
                        },{
                            name:'魔术',
                            value:50.0
                        },{
                            name:'活塞',
                            value:39.1
                        },{
                            name:'黄蜂',
                            value:36.0
                        },{
                            name:'公牛',
                            value:33.3
                        },{
                            name:'奇才',
                            value:31.8
                        },{
                            name:'老鹰',
                            value:26.1
                        },{
                            name:'骑士',
                            value:22.7
                        },{
                            name:'尼克斯',
                            value:17.4
                        }
                    ],
                    rowNum:7,
                    waitTime:1500,
                    unit:"%"
                },
                config2:{
                    data:[
                        {
                            name:'雄鹿',
                            value:87
                        },{
                            name:'凯尔特人',
                            value:76.2
                        },{
                            name:'热火',
                            value:73.9
                        },{
                            name:'76人',
                            value:70.8
                        },{
                            name:'猛龙',
                            value:68.2
                        },{
                            name:'步行者',
                            value:65.2
                        },{
                            name:'篮网',
                            value:56.5
                        },{
                            name:'魔术',
                            value:50.0
                        },{
                            name:'活塞',
                            value:39.1
                        },{
                            name:'黄蜂',
                            value:36.0
                        },{
                            name:'公牛',
                            value:33.3
                        },{
                            name:'奇才',
                            value:31.8
                        },{
                            name:'老鹰',
                            value:26.1
                        },{
                            name:'骑士',
                            value:22.7
                        },{
                            name:'尼克斯',
                            value:17.4
                        }
                    ],
                    rowNum:7,
                    waitTime:1500,
                    unit:"%"
                }
            }
        }

    }
</script>

<style lang="less">
  .left-chart{
    width: 100%;
    height: 100%;
    display: flex;
    flex-grow: 0;
    flex-direction: column;

    .lc-header{
      text-align: center;
      height: 40px;
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 30px;
      /*margin-bottom: 20px;*/
    }

    .lc-list{
      height: 100%;
      .lc-list-dongbu{
        width:100%;
        height:50%;
        .list-dongbu-content{
          padding:10px;
          font-size: 20px;
        }
        .list-dongbu{
          /*margin-bottom: px;*/
          width:100%;
          height:80%;
        }
      }

      .lc-list-xibu{
        width:100%;
        height:50%;
        .list-xibu-content{
          padding:10px;
          font-size: 20px;
        }
        .list-xibu{
          /*margin-bottom: px;*/
          width:100%;
          height:80%;
        }
      }


    }
  }

</style>

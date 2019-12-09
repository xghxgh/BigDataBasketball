<template>
<div class="right-chart">
  <div class="right-chart-list-top">
    <div class="players-message">
        <div class="players-name">
          勒布朗-詹姆斯
        </div>
        <div class="players-img">
          <img src="./img/james.png"/>
        </div>
    </div>
    <div class="players-shooting">
      <dv-active-ring-chart class="players-shooting-content":config="config" />
    </div>
  </div>
  <div class="right-chart-list-bottom">
    <div class="players-data">
      <dv-conical-column-chart :config="config1" />
    </div>
  </div>

</div>
</template>

<script>
    export default {
        name: "RightChart",
        data(){
            return{
                config:{
                    data:[
                        {
                            name:'投篮命中率',
                            value:50.1
                        },
                        {
                            name:'三分命中率',
                            value:36.4
                        },
                        {
                            name:'罚球命中率',
                            value:70.1
                        }
                    ],
                    lineWidth:30,
                    digitalFlopStyle:{
                        fontSize:20
                    }
                },
                config1:{
                    data:[
                        {
                            name:'投篮',
                            value:49
                        },
                        {
                            name:'投篮',
                            value:34
                        },
                        {
                            name:'投篮',
                            value:23
                        },
                        {
                            name:'投篮',
                            value:34
                        },
                        {
                            name:'投篮',
                            value:56
                        },
                    ],
                    showValue:true,
                }
            }
        }
    }
</script>

<style lang="less">
  .right-chart{
    display: flex;
    flex-direction: column;
    width: 100%;
    height: 100%;
    .right-chart-list-top{
      height: 50%;
      width: 100%;
      display: flex;
      flex-direction: row;
    }
    .right-chart-list-bottom{
      height: 50%;
      width: 100%;
    }
    .players-message{
      display: flex;
      flex-direction: column;
      width: 45%;
      .players-name{
        float: left;
        padding-left: 10px;
        margin-bottom: 5px;
        text-align:left;
        font-size: 30px;
        float: left;
        height: 40px;
      }
      .players-img img{
        padding-left: 20px;
        float: left;
        width: 70px;
        height: 100px;
      }
    }
    .players-shooting{
      height: 100%;
      width: 55%;
    }
    .players-shooting-content{
      width: 100%;
      height: 100%;
    }
    .players-data{
      width: 100%;
      height: 100%;
      /*padding-bottom: 30px;*/
      /*margin-bottom: 30px;*/
    }
  }

</style>

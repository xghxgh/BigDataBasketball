<template>
<div id="data-view">
  <dv-full-screen-container>
    <div class="main-header">
      <div class="mh-middle">篮球大数据系统</div>
    </div>

    <dv-border-box-1 class="main-container">
      <dv-border-box-4 :reverse="true" class="left-mian-content">
        <!--页面左侧内容-->

      </dv-border-box-4>

      <div class="right-mian-content">
        <!--页面右侧主体-->
        <div class="right-top-container">
          <!--页面左侧中上半部分-->
          <dv-border-box-3 class="letf-detail-content">
            <!--页面左侧中上半部分——左侧详细内容-->
          </dv-border-box-3>
          <dv-border-box-2 class="right-detail-content">
            <!--页面左侧中上半部分——右侧详细内容-->
          </dv-border-box-2>
        </div>
        <dv-border-box-2 class="right-bottom-container">
          <!--页面左侧中下半部分-->
        </dv-border-box-2>
      </div>
    </dv-border-box-1>

  </dv-full-screen-container>
</div>
</template>

<script>
  import DataV from '@jiaminghi/data-view';
  import Vue from 'vue'
  import BottomChart from "./BottomChart";
  import CenterCmp from "./CenterCmp";
  import LeftChart from "./LeftChart";
  import RightChart from "./RightChart";
  Vue.use(DataV)
    export default {
        name: "Index",
        components: {
            BottomChart,
            RightChart,
            LeftChart,
            CenterCmp
        },
        data(){
            return{
                msg:'hello index'
            }
        }
    }
</script>

<style lang="less">
#data-view{
  height: 100%;
  width: 100%;
  background-color: black;
  color: coral;
  #dv-full-screen-container{
    background-image: url("./img/timg.png");
    background-size: 100% 100%;
    box-shadow: 0 0 3px blue;
    display: flex;
    flex-direction: column;
  }
  .main-header{
    height: 80px;
    display: flex;
    justify-content: space-around;
    align-items: flex-end;
    .mh-middle{
      /*color: blue;*/
      font-size: 50px;
    }
  }
  .main-container{
    height: calc(~"100% - 80px");
    .border-box-content {
      padding: 5px;
      box-sizing: border-box;
      display: flex;
    }
  }

  .left-mian-content{
    width: 22%;
    padding: 4px;
    box-sizing: border-box;
  }
  .right-mian-content{
    width: 78%;
    padding-left: 1px;
    box-sizing: border-box;
  }
  .right-top-container{
    height: 60%;
    display: flex;
  }
  .right-bottom-container{
    height: 40%;
  }
  .letf-detail-content{
    width: 50%;
  }
  .right-detail-content{
    width: 50%;
  }
}

</style>

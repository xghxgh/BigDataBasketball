<template>
<div class="center-cmp">
  <div class="center-cmp-header">历史得分排行榜</div>
  <div class="center-cmp-list">
    <dv-capsule-chart class="center-cmp-list":config="config"  />
  </div>
</div>
</template>

<script>
    export default {
        name: "CenterCmp",
        data(){
            return{
                config:{
                    data:[
                        {
                            name: '贾巴尔',
                            value: 38387
                        },
                        {
                            name: '马龙',
                            value: 36928
                        },
                        {
                            name: '科比',
                            value: 33643
                        },
                        {
                            name: '詹姆斯',
                            value: 33132
                        },
                        {
                            name: '乔丹',
                            value: 32292
                        },
                        {
                            name: '诺维斯基',
                            value: 31560
                        },
                        {
                            name: '张伯伦',
                            value: 31419
                        },
                        {
                            name: '奥尼尔',
                            value: 28596
                        },
                        {
                            name: '海耶斯',
                            value: 27313
                        }
                    ],
                }
            }
        }
    }
</script>

<style lang="less">
  .center-cmp{
    width: 100%;
    height: 100%;
    .center-cmp-header{
      padding-top: 10px;
      width: 100%;
      height: 30px;
      font-size: 30px;
    }
    .center-cmp-list{
      padding-top: 20px;
      width: 100%;
      height: auto;
    }
  }

</style>

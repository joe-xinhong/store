<template>
    <div>
        <div v-if="kk==1">
            <GoodList :goodId="1"></GoodList>
        </div>
        <div v-else-if="kk==2">
            <GoodList :goodId="2"></GoodList>
        </div>
        <div v-else-if="kk==3">
            <GoodList :goodId="3"></GoodList>
        </div>
        <div v-else-if="kk==4">
            <GoodList :goodId="4"></GoodList>
        </div>
        <div v-else-if="kk==5">
            <GoodList :goodId="5"></GoodList>
        </div>
        <div v-else-if="kk==6">
            <GoodList :goodId="6"></GoodList>
        </div>
        <div v-else-if="kk==7">
            <GoodList :goodId="7"></GoodList>
        </div>
        <div v-else>
            <GoodList :goodId="0"></GoodList>
        </div>
    </div>
</template>
<script type="text/javascript" >
    import Msg from './Msg.js'
    import GoodList from './GoodList'
    export default {
        data(){
          return {
              kk:0
          }
        },
        mounted:function () {
            var _this = this
            /*接收值*/
            Msg.$on("val",function (m) {
                _this.kk = m;
            })
        },
        components: {
            GoodList
        }
    }
</script>
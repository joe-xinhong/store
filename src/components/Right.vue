<template>
    <div>
        <div v-if="kk==1">
            11111
        </div>
        <div v-if="kk==2">
            22222
        </div>
        <div v-if="kk==3">
            33333
        </div>
        <div v-if="kk==4">
            44444
        </div>
    </div>
</template>
<script type="text/javascript" >
    import Msg from './Msg.js'
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
        }
    }
</script>
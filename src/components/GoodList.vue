<template>
    <div class="show">
        <ul class="goodList">
            <li v-bind:key="good.id" v-for="good in list">
                <img v-bind:src="good.heardImg"/>
                <p>{{good.name}}</p>
                <p class="nike">{{good.nikeName}}</p>
            </li>
        </ul>
    </div>
</template>
<style type="text/css">
    .goodList li{
        list-style: none;
        width: 100px;
        height: 130px;
        float: left;
        font-size: 9px;
        color: red;
        margin-bottom: 30px;
    }
    .nike{
        color: blueviolet;
    }
    .goodList img{
        width: 90px;
        height: 90px;
    }
</style>
<script type="text/javascript">
    export default {
        name:"show",
        data(){
            var obj = this;
            var url = "";
            var lei = "";
            if (obj.goodId == 1){
                url="http://127.0.0.1:9000/hero/getPosition";
            }else if(obj.goodId == 2){
                url="http://127.0.0.1:9000/hero/getPosition";
                lei="坦克";
            }else if(obj.goodId == 3){
                url="http://127.0.0.1:9000/hero/getPosition";
                lei="战士";
            }else if(obj.goodId == 4){
                url="http://127.0.0.1:9000/hero/getPosition";
                lei="刺客";
            }else if(obj.goodId == 5){
                url="http://127.0.0.1:9000/hero/getPosition";
                lei="法师";
            }else if(obj.goodId == 6){
                url="http://127.0.0.1:9000/hero/getPosition";
                lei="射手";
            }else if(obj.goodId == 7){
                url="http://127.0.0.1:9000/hero/getPosition";
                lei="辅助";
            }else{
                url="http://127.0.0.1:9000/hero/getPosition";
            }
            if (lei!=""){
                this.$http.get(url+"?position="+lei).then(function (res) {
                    obj.list = res.data.data;
                })
            } else {
                this.$http.get(url).then(function (res) {
                    obj.list = res.data.data;
                })
            }

            return{
                list:[]
            }
        },
        props:{
            goodId:Number
        },
        watch:{ //监听goodId变化
            goodId(){
                var obj = this;
                var url = "";
                var lei = "";
                if (obj.goodId == 1){
                    //url="/json/cike.json";
                    url="http://127.0.0.1:9000/hero/getPosition";
                }else if(obj.goodId == 2){
                    url="http://127.0.0.1:9000/hero/getPosition";
                    lei="坦克";
                }else if(obj.goodId == 3){
                    url="http://127.0.0.1:9000/hero/getPosition";
                    lei="战士";
                }else if(obj.goodId == 4){
                    url="http://127.0.0.1:9000/hero/getPosition";
                    lei="刺客";
                }else if(obj.goodId == 5){
                    url="http://127.0.0.1:9000/hero/getPosition";
                    lei="法师";
                }else if(obj.goodId == 6){
                    url="http://127.0.0.1:9000/hero/getPosition";
                    lei="射手";
                }else if(obj.goodId == 7){
                    url="http://127.0.0.1:9000/hero/getPosition";
                    lei="辅助";
                }else{
                    url="http://127.0.0.1:9000/hero/getPosition";
                }
                if (lei!=""){
                    this.$http.get(url+"?position="+lei).then(function (res) {
                        obj.list = res.data.data;
                    })
                } else {
                    this.$http.get(url).then(function (res) {
                        obj.list = res.data.data;
                    })
                }
                return{
                    list:[]
                }
            }
        }
    }
</script>
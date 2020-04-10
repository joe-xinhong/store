<template>
    <div class="show">
        <ul class="goodList">
            <li v-bind:key="good.name" v-for="good in list">
                <img v-bind:src="good.img"/>
                <p>{{good.name}}</p>
            </li>
        </ul>
    </div>
</template>
<style type="text/css">
    .goodList li{
        list-style: none;
        width: 200px;
        height: 200px;
        float: left;
        font-size: 9px;
        color: red;
        margin-bottom: 30px;
    }
    .goodList img{
        width: 180px;
        height: 160px;
    }
</style>
<script type="text/javascript">
    export default {
        name:"show",
        data(){
            var obj = this;
            var url = "";
            if (obj.goodId == 1){
                url="/json/cike.json";
            }else if(obj.goodId == 2){
                url="/json/sheshou.json";
            }else {
                url="/json/sheshou.json";
            }
            this.$http.get(url).then(function (res) {
                obj.list = res.data;
                console.log(res)
            })
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
                if (obj.goodId == 1){
                    url="/json/cike.json";
                }else if(obj.goodId == 2){
                    url="/json/sheshou.json";
                }else {
                    url="/json/sheshou.json";
                }
                this.$http.get(url).then(function (res) {
                    obj.list = res.data;
                })
                return{
                    list:[]
                }
            }
        }
    }
</script>
<template>
    <div>
        <div class="title">新品推荐</div>
        <ul class="menu">
            <li @click="menu1" >全部</li>
            <li @click="menu2">坦克</li>
            <li @click="menu3">战士</li>
            <li @click="menu4">刺客</li>
            <li>法师</li>
            <li>射手</li>
            <li>辅助</li>
        </ul>
    </div>
</template>
<style type="text/css">
    .title{
        width: 100px;
        color: red;
    }
    .menu li{
        list-style: none;
        height: 80px;
        margin-bottom: 2px;
        background-color: white;
        line-height: 80px;
        cursor: pointer;
    }
</style>
<script type="text/javascript" >
    import Msg from './Msg.js'
    export default {
        methods:{
            menu1:function () {
                /*传值*/
                Msg.$emit("val","1");
            },
            menu2:function () {
                Msg.$emit("val","2");
            },
            menu3:function () {
                Msg.$emit("val","3");
            },
            menu4:function () {
                Msg.$emit("val","4");
            }
        }
    }
</script>
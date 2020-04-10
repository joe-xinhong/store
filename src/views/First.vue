<template>
    <div class="main">
        <div class="left">
            <Left></Left>
        </div>
        <div class="right">
            <div class="top">
                <img src="http://ossweb-img%2Eqq%2Ecom/upload/webplat/info/yxzj/20200408/96961325570770%2Ejpg"/>
            </div>
            <div class="bottom">
                <Right></Right>
            </div>
        </div>
    </div>
</template>

<script type="text/javascript" >
    import Left from '@/components/Left.vue'
    import Right from '@/components/Right.vue'
    export default {
        components: {
            Left,
            Right
        }
    }
</script>
<style type="text/css">
    *{
        padding: 0;
        margin: 0;
    }
    .left{
        width: 100px;
        float: left;
        margin-right: 10px;
    }
    .right{
        width: 1000px;
        float: left;
        margin-left: 10px;
    }
    .main{
        width: 1200px;
        margin: 20px auto;
    }
    .top img{
        height: 200px;
        width: 1000px;
    }
    .left,.right{
        background-color: #f5f5f5;
        height: 500px;
    }
</style>
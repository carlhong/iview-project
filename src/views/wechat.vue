<style>
    .wechat {
        padding: 40px 30px;
        text-align: center;
    }
    .wechat img {
        display: block;
        width: 180px;
        padding: 50px 0;
        margin: 0 auto;
    }
    .wechat a {
        display: inline-block;
        width: 232px;
        margin-top: 45px;
        color: #fff;
        background-color: #0DB3A6;
        border-color: #0DB3A6;
        border-radius: 2px;
        cursor: pointer;
        height: 36px;
        line-height: 34px;
        text-align: center;
        font-size: 14px;
    }
    .wechat a:hover {
        color: #fff;
        background-color: #0ca599;
        border-color: #0ca599;
    }
</style>
<template>
    <div class="wechat">
        <img src="../images/login_wechat.png">
        <a href="https://open.work.weixin.qq.com/wwopen/sso/3rd_qrConnect?appid=wx9b3c77819130e35c&redirect_uri=https%3A%2F%2Fwww.jiandaoyun.com%2Fwechat%2Fcorp%2Fauth&usertype=member">点击扫码登录</a>
    </div>
</template>
<script>
    export default {}
</script>
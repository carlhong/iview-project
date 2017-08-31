<style>
    .ding {
        padding: 25px 30px;
    }
    .ding .ivu-card-body {
        margin: auto;
        margin-top: 40px;
        text-align: center;
    }
    .ding .login_qrcode_text {
        margin-top: 20px;
        text-align: center;
        color: #898d90;
        font-size: 14px;
    }
    .ding .signin-tip {
        margin-top: 25px;
    }
    .ding a, .ding a:hover {
        color: #0DB3A6;
    }

</style>
<template>
    <div class="ding">
        <Card disHover>
            <div class="login_qrcode_content">
                <img src="../images/qrcode.png">
                <div class="login_qrcode_text">请使用钉钉扫描二维码登录</div>
            </div>
        </Card>
        <div class="signin-tip">
            <span>还未开通钉钉版？点此</span>
            <a href="https://www.jiandaoyun.com/register">立即开通</a>
        </div>
    </div>
</template>
<script>
    export default {}
</script>
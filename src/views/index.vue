<style>
    .account-pane {
        width: 400px;
        margin: 100px auto 40px auto;
    }
    .account-logo {
        padding: 15px;
        display: block;

    }
    .account-logo >img {
        margin: 0 auto;
        height: 40px;
        display: block;
    }
    .login-container {
        box-shadow: 0 0 6px rgba(0,0,0,.1);

    }
    .account-pane .ivu-card-body {
        padding: 0;
    }
    .account-pane .ivu-tabs-nav {
        float: none;
        line-height: 60px;
    }
    .account-pane .ivu-tabs-nav .ivu-tabs-tab {
        width: 30%;
        margin: 0 1.5%;
        text-align: center;

    }
    .account-pane  .ivu-tabs-nav .ivu-tabs-tab-active {
        color: #0DB3A6;
    }
    .account-pane  .ivu-tabs-nav .ivu-tabs-tab:hover {
        color: #0DB3A6;
    }
    .account-pane  .ivu-tabs-ink-bar {
        background-color: #0DB3A6;
    }
    .account-pane  .ivu-tabs-bar {
        margin-bottom: 0;
    }

</style>
<template>
    <div class="account-pane">
        <a href="https://www.jiandaoyun.com" class="account-logo">
            <img src="../images/logo-pure.png">
        </a>
        <Card class="login-container" dis-hover>
            <Tabs value="account">
                <Tab-pane label="帐号登录" name="account">
                    <Account></Account>
                </Tab-pane>
                <Tab-pane label="钉钉登录" name="dingding">
                    <DingDing></DingDing>
                </Tab-pane>
                <Tab-pane label="企业微信登录" name="wechat">
                    <WeChat></WeChat>
                </Tab-pane>
            </Tabs>
        </Card>
    </div>
</template>
<script>
    import Account from './account.vue';
    import DingDing from './dingding.vue';
    import WeChat from './wechat.vue';
    export default {
        components: {
            Account,
            DingDing,
            WeChat
        }
    }
</script>

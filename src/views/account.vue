<style>
    .account {
        padding: 30px 40px;
    }
    .account a, .account a:hover {
        color: #0DB3A6;
    }
    .account .ivu-form-item-content {
        margin: 0;
    }
    .account .ivu-input:focus, .account .ivu-input:hover {
        border-color: #0DB3A6;
    }
    .account .ivu-form-item {
        margin-bottom: 15px;
    }
    .account .ivu-btn-primary {
        background-color: #0DB3A6;
        border-color: #0DB3A6;
    }
    .signin-tip {
        text-align: center;
        font-size: 12px;
    }
    .split-line {
        font-size: 12px;
        text-align: center;
        margin: 30px 0 20px 0;
        height: 1px;
        border-top: 1px solid #e0e0e0;
    }
    .split-line span {
        color: #e0e0e0;
        position: relative;
        padding: 0 10px;
        top: -9px;
        background: #fff;
    }
    .other-account-list {
        font-size: 26px;
        height: 45px;
        padding: 0 15px;
    }
    .other-account-list i {
        color: #989898;
        border: solid 1px #e0e0e0;
        border-radius: 50%;
        position: relative;
        float: left;
        left: 0;
        margin: 0 13px;
        width: 45px;
        height: 45px;
        line-height: 45px;
        text-align: center;
        cursor: pointer;
    }
</style>
<template>
    <Form class="account" ref="formValidate" :model="formValidate" :rules="ruleValidate">
        <FormItem prop="name">
            <Input v-model="formValidate.name" placeholder="用户名/手机号码/邮箱"></Input>
        </FormItem>
        <FormItem prop="password">
            <Input type="password" v-model="formValidate.password" placeholder="密码"></Input>
        </FormItem>
        <Form-item>
            <Checkbox v-model="remember">下次自动登录</Checkbox>
            <a style="float:right" href="https://www.jiandaoyun.com/password/forget">忘记密码了？</a>
        </Form-item>
        <FormItem>
            <Button type="primary" long @click="handleSubmit('formValidate')">登录</Button>
        </FormItem>
        <div class="signin-tip">
            <span>还没有简道云账号？</span>
            <a href="https://www.jiandaoyun.com/register">立即注册</a>
        </div>
        <div class="split-line">
            <span>使用其他账号登录</span>
        </div>
        <div class="other-account-list">
            <Icon type="more"/>
            <Icon type="more"/>
            <Icon type="more"/>
            <Icon type="more"/>
        </div>
    </Form>
</template>
<script>
    export default {
        data () {
            return {
                formValidate: {
                    name: '',
                    password: ''
                },
                ruleValidate: {
                    name: [
                        { required: true, message: '帐号不能为空', trigger: 'blur' }
                    ],
                    password: [
                        { required: true, message: '密码不能为空', trigger: 'blur' }
                    ]
                }
            }
        },
        methods: {
            handleSubmit (name) {
                this.$refs[name].validate((valid) => {
                    if (valid) {
                        this.$Message.success('提交成功!');
                    } else {
                        this.$Message.error('表单验证失败!');
                    }
                })
            }
        }
    }
</script>

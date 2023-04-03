<template>
  <div class="login">
    <el-form class="login-form">
      <h3 class="title">管理系统</h3>
      <el-form-item>
        <el-input type="text" placeholder="账号" v-model="loginForm.username" />
      </el-form-item>
      <el-form-item>
        <el-input type="password" placeholder="密码" v-model="loginForm.password" />
      </el-form-item>
      <el-form-item>
        <el-input style="width:63%" placeholder="验证码"  v-model="loginForm.code" />
        <div class="login-code">
          <img :src="codeUrl" class="login-code-img"/>
        </div>
      </el-form-item>
      <el-checkbox v-model="loginForm.rememberMe" style="margin:0px 0px 25px 0px;">记住密码</el-checkbox>
       <el-form-item style="width:100%">
        <el-button type="primary" style="width:100%">
          <span>登录</span>
        </el-button>
       </el-form-item>
    </el-form>
    <div class="el-login-footer">
      <span>Copyright © 2018-2023 ruoyi.vip All Rights Reserved.</span>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      codeUrl: "",
      loginForm: {
        username: "",
        password: "",
        rememberMe: false,
        code: "",
      },
    }
  }
}
</script>

<style >
.login{
  height: 100%;
  background-image: url('~@/assets/images/login-background.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  display: flex;
  justify-content: center;
  align-items: center;
}
.login-form{
  width: 400px;
  background-color: pink;
  padding: 25px 25px 5px 25px;
}
.el-login-footer{
  position: fixed;
  bottom: 0;
  color: #fff;
  font-size: 12px;
  letter-spacing: 1px;
  font-family: Arial;
}
.login-code{
  width: 33%;
  float:right;
}
</style>
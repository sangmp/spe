<template>
  <div id="app">
    <div class="header"></div>
    <div class="content">
    <el-form class="form" label-width="110px">
      <el-tabs v-model="registerType">
        <el-tab-pane name="mobile">
          <span slot="label">手机号码注册</span>
          <el-form-item label="手机号码">
            <el-input v-model="mobile" placeholder="请输入手机号码"></el-input>
          </el-form-item>
          <el-form-item label="短信验证码">
            <el-row>
              <el-col :span="14">
                <el-input v-model="smsCode" placeholder="请输入短信验证码"></el-input>
              </el-col>
              <el-col :span="9" :offset="1">
                <el-button type="info" style="width:100%">获取验证码</el-button>
              </el-col>
            </el-row>
          </el-form-item>
        </el-tab-pane>
        <el-tab-pane name="email">
          <span slot="label">邮箱注册</span>
          <el-form-item label="邮箱地址">
            <el-input v-model="email" placeholder="请输入邮箱地址"></el-input>
          </el-form-item>
        </el-tab-pane>
      </el-tabs>
      <el-form-item label="验证码">
        <el-row>
          <el-col :span="14">
            <el-input v-model="imgCode" placeholder="请输入验证码"></el-input>
          </el-col>
          <el-col :span="9" :offset="1">
            <el-button type="info" style="width:100%">获取验证码</el-button>
          </el-col>
        </el-row>
      </el-form-item>
      <el-form-item label="密码">
        <el-input v-model="password" placeholder="请输入密码"></el-input>
      </el-form-item>
      <el-form-item label="确认密码">
        <el-input v-model="confirmPassword" placeholder="请在此输入密码"></el-input>
      </el-form-item>
      </el-form>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      registerType: 'mobile',
      mobile: '',
      email: '',
      smsCode: '',
      imgCode: '',
      password: '',
      confirmPassword: ''
    }
  },

  methods: {
  }
}
</script>

<style>
body {
  font-family: Helvetica, sans-serif;
}
.header{

}
.content{
  width: 640px;
  margin-left: auto;
  margin-right: auto;
}
.form{
  width: 400px;
  margin-left: auto;
  margin-right: auto;
}
</style>

<template>
  <div class="login">
      <input type="text" v-model="username" placeholder="请输入用户名">
      <input type="password" v-model="password" placeholder="请输入密码">
      <div class="login_btn" @click='login'>登录</div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      username: '',
      password: ''
    }
  },
  methods:{
    login(){
      if(this.username == '' && this.password == ''){
        alert('请输入用户名密码')
        return
      }
      if(this.username != 'ming' || this.password != '123123'){
        alert('用户名密码错误')
        return
      }
      this.$router.push({name:'index'})
    }
  }
}
</script>

<style scoped>
    .login{width: 100%;height: 100%;background: url(../assets/images/login_bg.jpg) no-repeat center center;background-size: 100% 100%;display: flex;justify-content: center;align-items: center;flex-direction: column;}
    .login input{background-color: transparent;border-bottom: 1px solid #d2d2d2;line-height: 1.44rem;width: 7.33rem;text-indent: .2rem;}
    .login_btn{width: 5.73rem;font-size: .4rem;background-color: #c4e3e5;text-align: center;border-radius: .5rem;color: #fff;margin-top: 1.87rem;line-height: 1rem;}
</style>
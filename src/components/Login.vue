<template>
  <div class="mainDiv">
    <div class="login_top">
      <div class="login_system">
        <span><img src="../assets/images/zksecurity_zh_CN.png" class="login_logo"></span>
      </div>
    </div>
    <div class="login">
      <form id="empLoginForm" method="post">
        <div>
          <input type="text" id="userName" class="login_inp" placeholder="用户名" v-model="userName"/>
          <br>
          <input type="password" id="password" class="login_inp" placeholder="密码" v-model="password">
          <br>
          <input type="button"  value="登录" class="login_button login_ok" v-on:click="submit"/>
          <input type="button" name="cancel" value="取消" class="login_button login_cancel">
        </div>
      </form>
    </div>
    <div class="login_bottom">
      <span><img src="../assets/images/logo.png" class="logo"></span>
    </div>
  </div>
</template>

<script>

export default {
  name: 'login',
  data() {
    return {
      userName :'',
      password : '',
      error :'账号密码不可为空'
    }
  },
  methods : {
    submit :function() {
      if (this.userName == '' || this.password == '')
      {
        alert(this.error);
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

span {
  height: 100%;
  display: inline-block;
  vertical-align: middle;
}
.mainDiv{
  height: 100%;
  width: 100%;
  margin : 0;
}
.login_inp{
  border: 1px solid #7ac143;
  font-size: 15px;
  line-height: 46px;
  border-radius: 3px;
  height: 46px;
  width: 384px;
  margin-top: 30px;
  color: #777c80;
  padding-top: 0px;
  padding-right: 8px;
  padding-bottom: 0px;
  padding-left: 8px;
  height: 46px;
}

.login_top {
  height: 20%;
  width: 100%;
  margin: 0;
  background-color: #474b4f;
}

.login_logo {
  width: 255px;
  height: 52px;
  vertical-align: middle;
  margin-top: 15%;
}

.login_system {
  text-align: center;
  font-size: 50px;
  line-height: 46px;
  vertical-align: middle;
}

.login{
  height: 50%;
  width: 100%;
  margin-top: auto;
  background-color: #78b847;
}

.login_button{
  font-size: 16px;
  font-weight: bold;
  color: #FFFFFF;
  background-repeat: no-repeat;
  background-position: left;
  height: 48px;
  background-color: #474b4f;
  text-align: left;
  /* padding-left: 60px; */
  text-indent: 60px;
  border: 1px solid #FFFFFF;
  border-radius: 3px;
  cursor: pointer;
  margin-top: 30px;
}

.login_ok{
  background-image: url(../assets/images/button2.png);
  min-width: 130px;
  margin-right: 130px;
}
.login_cancel{
  
  background-image: url(../assets/images/fing_disabled.png);
  min-width: 130px;
}

.login_bottom{
  height: 20%;
  width: 100%;
  margin: 0;
  background-color: #474b4f;
}
.logo{
  vertical-align: middle;
  margin-top: 40%;
}

</style>

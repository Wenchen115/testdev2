<template>
  <div class="login">
    <div class="main-head">
      <div class="head-img">
        <img :src ='vueImg' height="50px" width="50px"/>
        <span>接口测试系统</span>
      </div>
    </div>

    <div class="login-context">
      <h2>账号登陆</h2>
      <div>
        <el-input v-model="loginForm.name" placeholder="请输入用户名"></el-input>
        <el-input placeholder="请输入密码" v-model="loginForm.passWord" show-password></el-input>
      </div>

      <div class="login-button-class">
        <el-button type="success" @click="login">登陆</el-button>
        <el-button type="danger" @click="register">注册</el-button>


      </div>
    </div>
  </div>
</template>

<script>
  import img from "../assets/logo.png"
  export default {
    name:'login',
    components:{

    },
    props:{

    },
    data(){
      return{
        vueImg:img,

        loginForm:{
          name:"",
          passWord:"",
        }

      }
    },
    methods:{

    },
    created() {
    }
  }

</script>

<style scoped>
。main-head{
  background: #eff4fa;
  height: 60px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 20px;
}

.head-img{
  display: flex;
  align-items: center;
}

.login-context{
  width: 400px;
  margin-left: auto;
  margin-right: auto;
  border-radius: 2px;
  border: 1px solid #a0b1c4;

  margin-top: 50px;

  padding: 10px 30px;

}

.login-button-class{
  display: flex;
  justify-content: space-between;
  padding-left: 25px;
}
</style>
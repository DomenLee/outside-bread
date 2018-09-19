<template>
  <div class="page-wrap-flex">
    <van-nav-bar
      title="登录"
      left-arrow
    />
    <div class="page-content-flex-item">
      <van-cell-group>
        <van-field
          v-model="username"
          required
          clearable
          label="用户名"
          placeholder="请输入用户名"
        />

        <van-field
          v-model="password"
          type="password"
          label="密码"
          placeholder="请输入密码"
          required
        />
      </van-cell-group>
      <van-button class="submit-btn" size="large" type="primary" @click="sign">登录</van-button>
      <router-link to='/register' class='tip'>注册</router-link>
    </div>
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

  methods: {
    sign () {
      this.$router.push('/home')
    }
  }
}
</script>

<style lang='less' scoped>
.page-content-flex-item {
  .van-cell-group {
    margin-top: 10px;
  }
  .submit-btn {
    margin-top: 10px;
  }
  .tip {
    display: block;
    margin: 10px;
  }
}
</style>

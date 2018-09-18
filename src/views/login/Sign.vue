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
      <van-button class="submit-btn" size="large" type="primary">登录</van-button>
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
    submit () {}
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
}
</style>

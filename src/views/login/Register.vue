<template>
  <div class="page-wrap-flex">
    <van-nav-bar
      title="注册"
      left-arrow
    />
    <div class="page-content-flex-item">
      <van-steps :active="active">
        <van-step>输入手机号</van-step>
        <van-step>输入验证码</van-step>
        <van-step>设置密码</van-step>
      </van-steps>
      <div class="fisrt-box" v-if='active === 0'>
        <van-cell-group>
          <van-field v-model="phone" type='tel' placeholder="请输入手机号" />
        </van-cell-group>
        <div class="btn-wrap">
          <van-button class="submit-btn" size="large" type="primary" @click='active = 1'>获取验证码</van-button>
        </div>
      </div>
      <div class="tow-box" v-if='active === 1'>
        <van-cell-group>
          <van-field v-model="code" type='text' placeholder="请输入验证码" />
        </van-cell-group>
        <div class="btn-wrap">
          <van-button class="submit-btn" size="large" type="primary" @click='active = 2'>设置密码</van-button>
        </div>
      </div>
      <div class="three-box" v-if='active === 2'>
        <van-cell-group>
          <van-field v-model="code" type='text' placeholder="请输入验证码" />
        </van-cell-group>
        <div class="btn-wrap">
          <van-button class="submit-btn" size="large" type="primary">完成</van-button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      active: 0,
      phone: '',
      code: '',
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
    margin: 10px 0;
  }
}
.btn-wrap {
  padding: 0 10px;
}
</style>

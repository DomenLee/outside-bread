<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style lang='less'>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.page-wrap-flex {
  display: flex;
  flex-direction: column;
  height: 100vh;
}

.page-content-flex-item {
  flex: 1;
  overflow-y: scroll;
  overflow-x: hidden;
  background-color: #f9f9f9;
}

a.tip {
  color: #999;
  font-size: 14px;
}
</style>

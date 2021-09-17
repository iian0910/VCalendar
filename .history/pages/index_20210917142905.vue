<template>
  <div class="container">
    <div class="input" @click="drawer = true"></div>

    <!-- drawer -->
    <el-drawer
      title="我是标题"
      :visible.sync="drawer"
      :direction="direction"
    >
      <span>我来啦!</span>
    </el-drawer>
  </div>
</template>

<script>
export default {
  data () {
    return {
      drawer: false,
      direction: 'btt'
    }
  }
}
</script>

<style scoped>
.container {
  max-width: 400px;
}
.input {
  padding: 5px;
  width: 100%;
  border: 1px solid black;
}
</style>

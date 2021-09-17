<template>
  <div class="container">
    <el-input v-model="input" placeholder="请输入内容" @click="drawer = true"></el-input>

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
</style>

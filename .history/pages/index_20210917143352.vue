<template>
  <div class="container">
    <div @click="drawer = true">
      <el-input v-model="input" placeholder="请输入内容"></el-input>
    </div>

    <!-- drawer -->
    <el-drawer
      title="我是标题"
      :visible.sync="drawer"
      :direction="direction"
    >
      <v-date-picker
        :value="null"
        color="red"
        is-dark
        is-range
      />
    </el-drawer>
  </div>
</template>

<script>
export default {
  data () {
    return {
      drawer: false,
      direction: 'btt',
      input: ''
    }
  }
}
</script>

<style scoped>
.container {
  max-width: 400px;
}
</style>

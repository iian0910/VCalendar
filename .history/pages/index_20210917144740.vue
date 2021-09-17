<template>
  <div class="container">
    {{date}}
    <div @click="drawer = true">
      <el-input v-model="input" placeholder="请输入内容"></el-input>
    </div>

    <!-- drawer -->
    <el-drawer
      title="我是标题"
      :visible.sync="drawer"
      :direction="direction"
      size="auto"
    >
      <v-date-picker
        class="vCalendar"
        title-position="left"
        is-expanded
        v-model="date"
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
      input: '',
      date: new Date()
    }
  }
}
</script>

<style scoped>
.container {
  max-width: 400px;
}
.vCalendar {
  border: none;
}
</style>

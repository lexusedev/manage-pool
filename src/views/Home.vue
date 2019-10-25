<template>
  <el-container>
  <el-header>
    <navigate></navigate>
  </el-header>
  <el-container>
    <el-aside width="200px"></el-aside>
    <el-main></el-main>
  </el-container>
</el-container>
</template>

<script>
// @ is an alias to /src
import navigate from '@/components/layout/navigate'
export default {
  name: 'home',
  components: {
    navigate
  },
  data() {
    return {
      testVal: []
    }
  },
  methods: {
    init() {
      const vm = this
      vm.axios.get('/test')
        .then(res => {
          let data = res.data
          vm.testVal = data
          console.log(data)
        })
    }
  },
  mounted() {
    this.init()
  }
}
</script>

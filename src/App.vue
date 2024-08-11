<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <DataTable :jsonData="data"/> <!-- 使用 DataTable 组件 -->
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import DataTable from './components/DataTable.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    DataTable
  },
  data() {
    return {
      data:  [
        {
          Title: "房子坐北朝南的户型 里面的布局合理 采光好",
          PositionName: "光谷地产湾郡",
          HouseInfo: "2室2厅 | 86.44平米 | 南 北 | 精装 | 中楼层(共22层)  | 板楼",
          Price: "12,957元/平"
        },
        {
          Title: "都想买套低楼层采光好+单价总价优",
          PositionName: "三环南",
          HouseInfo: "2室1厅 | 64.99平米 | 南 北 | 其他 | 中楼层(共7层)  | 板楼",
          Price: "11,695元/平"
        },
        // 其他数据项...
      ]
    }
  }
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

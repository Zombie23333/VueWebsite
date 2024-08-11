<template>
    <div class="table-container">
      <table>
        <thead>
          <tr>
            <th v-for="key in keys" :key="key">{{ key }}</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(item, index) in jsonData" :key="index"><!-- 修改2：将 :key 从 item.id 改为 index，避免可能的 undefined 错误 -->
            <td v-for="(value, key) in item" :key="key">{{ value }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </template>
  
  <script>
  export default {
    props: ['jsonData'],
    computed: {
      keys() {
        return this.jsonData && this.jsonData.length > 0 ? Object.keys(this.jsonData[0]) : [];
      }
    }
  };
  </script>

<style scoped>
.table-container { 
  display: flex;
  justify-content: center; /* 水平居中 */
  align-items: center;     /* 垂直居中 */
  height: 100%;            /* 确保容器占满高度 */
}

table {
  width: auto;             /* 表格宽度自适应内容 */
  border-collapse: collapse;
}

th, td {
  border: 1px solid #ddd;
  padding: 8px;
}

th {
  background-color: #f2f2f2;
}
</style>
  
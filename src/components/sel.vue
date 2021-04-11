<template>
  <div class="content">
    <h1>vue+element ui可选可输入可搜索下拉列表</h1>
    <el-select v-model="content" filterable placeholder="请选择" @blur="selectBlur">
      <el-option v-for="(item,key,index) in options" :label="item.name" :value="item.name" :key="index">
      </el-option>
    </el-select>
  </div>
</template>

<script>
export default {
  data() {
    return {
      options: [
        { name: 'data1' },
        { name: 'data2' },
        { name: 'data3' },
        { name: 'data4' },
        { name: 'data5' },
        { name: 'data6' },
        { name: 'data7' },
        { name: 'data8' },
      ],
      content: null,
    }
  },
  methods: {
    selectBlur(event) {
      this.inputContent = event.target.value
    },
  },
}
</script>
<style scoped lang="scss"></style>

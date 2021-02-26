<template>
  <div class="container">
    <div class="tree-part">
      <el-input
        class="search"
        placeholder="请选择查询名称"
      />
      <el-tree
        style="overflow: scroll;height: 100%;"
        :data="treeData"
        :props="defaultProps"
        @node-click="handleNodeClick"
      />
    </div>
    <div class="table-part">
      <el-table
        :data="tableData"
        style="width: 100%"
      >
        <el-table-column
          prop="date"
          label="属性1"
          width="180"
        />
        <el-table-column
          prop="name"
          label="属性2"
          width="180"
        />
        <el-table-column
          prop="address"
          label="属性3"
          width="180"
        />
      </el-table>
    </div>
  </div>
</template>

<script>
export default {
  name: 'System1',
  data() {
    return {
      treeData: [{
        label: '1',
        children: [{
          label: '1-1',
          children: [{
            label: '1-1-1',
            children: [{
              label: '1-1-1-1',
              children: [{
                label: '1-1-1-1-1',
                children: [{
                  label: '1-1-1-1-1-1'
                }]
              }]
            }]
          }]
        }, {
          label: '1-2',
          children: [{
            label: '1-2-1',
            children: [{
              label: '1-2-1-1',
              children: [{
                label: '1-2-1-1-1'
              }]
            }]
          }]
        }, {
          label: '1-3',
          children: [{
            label: '1-3-1',
            children: [{
              label: '1-3-1-1',
              children: [{
                label: '1-3-1-1-1'
              }]
            }]
          }]
        }, {
          label: '1-3',
          children: [{
            label: '1-3-1',
            children: [{
              label: '1-3-1-1',
              children: [{
                label: '1-3-1-1-1'
              }]
            }]
          }]
        }, {
          label: '1-3',
          children: [{
            label: '1-3-1',
            children: [{
              label: '1-3-1-1',
              children: [{
                label: '1-3-1-1-1'
              }]
            }]
          }]
        }]
      }],
      defaultProps: {
        children: 'children',
        label: 'label'
      },
      tableData: [{
        date: '2016-05-02',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1518 弄'
      }, {
        date: '2016-05-04',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1517 弄'
      }, {
        date: '2016-05-01',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1519 弄'
      }, {
        date: '2016-05-03',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1516 弄'
      }]
    }
  },
  computed: {
    // ...mapGetters([
    //   'name',
    //   'avatar',
    //   'roles'
    // ])
  },
  created() {
  },
  methods: {
    handleNodeClick(data) {
      console.log(data)
    }
  }
}
</script>
<style scoped>
    .container {
        margin: 7%;
        display: flex;
        justify-content: center;
    }
    .tree-part {
      height: 300px;
    }
    .search {
      margin-bottom: 5%;
    }
    .table-part{
      margin-left: 15%;
    }
</style>

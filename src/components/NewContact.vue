<template>
  <el-row>
    <el-col :xs="24" :sm="18" :md="14" :lg="10" id="main">
      <label>姓名: </label> {{ info.name }}
      <el-input v-model="info.name" placeholer="请输入姓名"></el-input>
      <label>年龄: </label> {{ info.age }}
      <el-input v-model="info.age" placeholer="请输入年龄"></el-input>
      <label>性别: </label> {{ info.sex }}
      <el-select v-model="info.sex" placeholder="请选择性别">
        <el-option
          v-for="item in options"
          :key="item"
          :value="item"
        ></el-option>
      </el-select>
      <el-button class="btn-auto" @click="create" type="success"
        >创建</el-button
      >
      <template>
        <el-table :data="tabledata" align="left">
          <el-table-column prop="name" label="姓名"></el-table-column>
          <el-table-column prop="age" label="年龄"></el-table-column>
          <el-table-column prop="sex" label="性别"></el-table-column>
          <el-table-column label="操作">
            <template v-slot="dataScope">
              <el-button size="mini" type="danger" @click="del(dataScope)"
                >删除</el-button
              >
            </template>
          </el-table-column>
        </el-table>
      </template>
    </el-col>
  </el-row>
</template>

<script>
import Storage from "../store/store";
export default {
  name: "NewContact",
  data() {
    return {
      info: {
        name: "",
        age: null,
        sex: "",
      },
      options: ["女", "男", "保密"],
      //   tabledata: [
      //     { name: "Leo", age: 12, sex: "man" },
      //     { name: "Lei", age: 22, sex: "women" },
      //     { name: "Lii", age: 65, sex: "men" },
      //   ],
      tabledata: Storage.fetch(),
    };
  },
  methods: {
    create() {
      //   console.log(this);
      this.tabledata.push(this.info);
      this.resetInfo();
    },
    del(slotScopeData) {
      //   console.log(slotScopeData);
      //   console.log(slotScopeData.$index);
      this.tabledata.splice(slotScopeData.$index, 1);
    },
    resetInfo() {
      this.info = {
        name: "",
        age: null,
        sex: "",
      };
    },
  },
  watch: {
    tabledata: {
      handler(items) {
        Storage.save(items);
      },
      deep: true,
    },
  },
};
</script>
<style lang="scss" scoped>
#main {
  float: none;
  margin: 0 auto;
}
.el-input {
  padding-bottom: 5px;
}
.el-select {
  display: block;
}
.btn-auto {
  width: 100%;
  margin-top: 12px;
  margin-bottom: 12px;
}
</style>
<template>
  <table
    id="test"
    border="1px"
    width="100%"
    cellspacing="0"
    cellpadding="0"
    align="center"
    bgcolor="#fff"
  >
    <thead>
      <tr>
        <th width="10%">调查案例</th>
        <th width="10%">公司名称</th>
        <th width="10%">地址</th>
        <th width="5%">部门</th>
        <th width="5%">联系人</th>
        <th width="10%">联系方式</th>
        <th width="20%">具體情况</th>
        <th width="20%">问券填写</th>
        <th width="10%">提交时间</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>1</td>
        <td>2</td>
        <td>3</td>
        <td>4</td>
        <td>5</td>
        <td>6</td>
        <td>7</td>
        <td>8</td>
        <td>9</td>
      </tr>
    </tbody>
  </table>
</template>

<script>
import table2excel from "js-table2excel";
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data() {
    return {
      column: [
        {
          title: "Name",
          key: "name",
          type: "text"
        },
        {
          title: "Pic",
          key: "pic",
          type: "image",
          width: 80,
          height: 50
        }
      ],
      data: [
        {
          name: "xiao",
          age: "18",
          pic: "https://profile.csdnimg.cn/9/8/3/2_xiaoxiaojie12321"
        },
        {
          name: "jie",
          age: "18",
          pic: "https://profile.csdnimg.cn/9/8/3/2_xiaoxiaojie12321"
        }
      ],
      excelName: 'test'
    };
  },
  mounted() {
    table2excel(this.column, this.data, this.excelName);
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>

<template>
  <div>
    <div id="mainbox">
      <div id="leftbox">
        <div id="left-topbox">
          {{ title }}
        </div>
        <div id="left-secbox">
          <div id="avatarbox">
            <el-avatar :size="150"></el-avatar>
          </div>
          <div id="namebox">
            {{ title }}
          </div>
          <div id="listbox">
            <el-table :data="tableData" class="table1">
              <el-table-column
                prop="article"
                label="文章"
                width="66"
                align="center"
              ></el-table-column>
              <el-table-column
                prop="class"
                label="分类"
                width="66"
                align="center"
              ></el-table-column>
              <el-table-column
                prop="comment"
                label="评论"
                width="66"
                align="center"
              ></el-table-column>
            </el-table>
          </div>
        </div>
        <div id="left-thrbox">
          导航
          <div class="mbox1">
            <div class="el-icon-house"></div>
            <a href="tosaka.cn">首页</a>
          </div>
          组成
          <div class="mbox1">
            <el-collapse>
              <el-collapse-item  title="分类" name="1">
                <a class="mbox2" href="1">默认分类</a>
                <a class="mbox2" href="1">默认分类2</a>
              </el-collapse-item>
              <el-collapse-item title="页面" name="2">
              </el-collapse-item>
            </el-collapse>
          </div>
        </div>
      </div>
      <div id="midbox"></div>
      <div id="rightbox"></div>
    </div>
  </div>
</template>

<style scoped>
#mainbox {
  position: absolute;
  width: 1000px;
  height: 880px;
  margin-left: 15%;
  margin-right: 15%;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.12), 0 0 6px rgba(0, 0, 0, 0.04);
}
#leftbox {
  position: relative;
  width: 200px;
  height: 100%;
  float: left;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.12), 0 0 6px rgba(0, 0, 0, 0.04);
}
#midbox {
  position: relative;
  width: 590px;
  height: 100%;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.12), 0 0 6px rgba(0, 0, 0, 0.04);
  float: left;
}
#rightbox {
  position: relative;
  width: 200px;
  height: 100%;
  float: right;
}
#left-topbox {
  height: 50px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.12), 0 0 6px rgba(0, 0, 0, 0.04);
  text-align: center;
}
#left-secbox {
  height: 300px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.12), 0 0 6px rgba(0, 0, 0, 0.04);
}
#avatarbox {
  margin: 10px 25px;
}
#namebox {
  text-align: center;
}
#left-thrbox {
  padding: 20px 5px;
  font-size: 15px;
  color: grey;
}
a:link {
  text-decoration: none;
}
.mbox1 {
  height: 30px;
  margin: 10px 1px;
  font-size: 17px;
  color: black;
}
.mbox1:hover {
  background-color: rgb(223, 222, 222);
  transition-duration: 500ms;
}
.mbox2 {
  height: 30px;
  font-size: 10px;
  display: block;
}
.mbox2:hover {
  background-color: rgb(223, 222, 222);
  transition-duration: 500ms;
}
.mbox2:link {
    color: grey;
}
</style>

<script lang="ts">
export default {
  data() {
    return {
      title: "GENG",
      tableData: [{ article: 1, class: 1, comment: 1 }],
    };
  },
};
</script>


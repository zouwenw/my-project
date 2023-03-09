<template>
  <div class="box">
    <div class="title">拖动右边把手排序</div>
    <ul class="sort-list" v-for="(item, index) in sortList" :key="index">
      <li class="list-item">
        <div class="item-wrap">
          <div class="index">{{ index + 1 }}</div>
          <div>{{ item.name }}</div>
        </div>
        <van-icon name="wap-nav" color="#ccc" size="20" />
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      sortList: [
        {
          name: "选项A",
        },
        {
          name: "选项B",
        },
        {
          name: "选项C",
        },
        {
          name: "选项D",
        },
      ],
    };
  },
};
</script>

<style scoped>
.box {
  padding: 0 20px;
}
.index {
  width: 20px;
  height: 20px;
  line-height: 20px;
  text-align: center;
  border-radius: 50%;
  background: #ccc;
  color: #fff;
  margin-right: 10px;
}
.title {
  color: #ccc;
  padding-bottom: 10px;
  border-bottom: 1px solid #ddd;
}
.item-wrap {
  display: flex;
  align-items: center;
}
.list-item {
  border-bottom: 1px solid #ddd;
  height: 50px;
  line-height: 50px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>

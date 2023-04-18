<template>
  <div class="leftbar">
    <div class="leftbar-search">
      <search-outlined />
      <input type="text" placeholder="Find..." />
      <span class="toolsbar-item"><close-outlined /></span>
    </div>
    <div class="leftbar-view">
      <div class="leftbar-view-item">Triangke</div>
      <div class="leftbar-view-item">Square</div>
      <div class="leftbar-view-item">Text1</div>
    </div>
  </div>
</template>

<script>
import { SearchOutlined } from "@ant-design/icons-vue";
import { CloseOutlined } from "@ant-design/icons-vue";

export default {
  name: "LeftBar",
  components: {
    SearchOutlined,
    CloseOutlined,
  },
};
</script>

<style scoped>
.leftbar {
  background: #ffffff;
  border-right: 1px solid #e6e6e6;
  height: 100%;
}

.leftbar-search {
  padding: 0 0 0 10px;
  border-bottom: 1px solid #e6e6e6;
}

.leftbar-search input {
  width: 195px;
  /*color: #e6e6e6;*/
  font-size: 12px;
  height: 30px;
  outline: none;
  border: 0;
  padding-left: 10px;
}

.toolsbar-item {
  padding: 1px 4px 2px 4px;
  font-size: 14px;
  cursor: pointer;
  border-radius: 3px;
}
.toolsbar-item:hover {
  background: #f5f5f5;
}
.leftbar-view-item {
  padding: 5px 10px;
  cursor: pointer;
  box-sizing: content-box;
  border: 1px solid #fff;
}
.leftbar-view-item:hover {
  border: 1px solid #41b883;
}
</style>

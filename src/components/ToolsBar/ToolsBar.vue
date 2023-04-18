<template>
  <div class="toolsbar">
    <span class="toolsbar-group">
      <span class="toolsbar-item"><save-outlined /></span>
    </span>
    <span class="toolsbar-group">
      <span class="toolsbar-item"><zoom-out-outlined /></span>
      <span class="toolsbar-item"><zoom-in-outlined /></span>
    </span>
    <span class="toolsbar-group">
      <span class="toolsbar-item"><swap-left-outlined /></span>
      <span class="toolsbar-item"><swap-right-outlined /></span>
    </span>
    <span class="toolsbar-group">
      <span class="toolsbar-item"><delete-outlined /></span>
    </span>
    <span class="toolsbar-group">
      <span class="toolsbar-item"><vertical-align-bottom-outlined /></span>
      <span class="toolsbar-item"><vertical-align-top-outlined /></span>
    </span>
    <span class="toolsbar-group">
      <span class="toolsbar-item"><edit-outlined /></span>
      <span class="toolsbar-item"><copy-outlined /></span>
      <span class="toolsbar-item"><scissor-outlined /></span>
    </span>

    <span class="toolsbar-group">
      <span class="toolsbar-item">
        <plus-outlined />
        <caret-down-outlined class="toolsbar-item-caret" />
      </span>
    </span>
  </div>
</template>

<script>
import { SaveOutlined } from "@ant-design/icons-vue";
import { ZoomInOutlined } from "@ant-design/icons-vue";
import { ZoomOutOutlined } from "@ant-design/icons-vue";
import { SwapLeftOutlined } from "@ant-design/icons-vue";
import { SwapRightOutlined } from "@ant-design/icons-vue";
import { DeleteOutlined } from "@ant-design/icons-vue";
import { VerticalAlignBottomOutlined } from "@ant-design/icons-vue";
import { VerticalAlignTopOutlined } from "@ant-design/icons-vue";
import { EditOutlined } from "@ant-design/icons-vue";
import { CopyOutlined } from "@ant-design/icons-vue";
import { ScissorOutlined } from "@ant-design/icons-vue";
import { PlusOutlined } from "@ant-design/icons-vue";
import { CaretDownOutlined } from "@ant-design/icons-vue";

export default {
  name: "ToolsBar",
  components: {
    SaveOutlined,
    ZoomInOutlined,
    ZoomOutOutlined,
    SwapLeftOutlined,
    SwapRightOutlined,
    DeleteOutlined,
    VerticalAlignBottomOutlined,
    VerticalAlignTopOutlined,
    EditOutlined,
    CopyOutlined,
    ScissorOutlined,
    PlusOutlined,
    CaretDownOutlined,
  },
};
</script>

<style scoped>
.toolsbar {
  background: #ffffff;
  margin: 0;
  padding: 3px 0;
  /*height: 40px;*/
  border-bottom: 1px solid #e6e6e6;
}

.toolsbar-group {
  border-left: 1px solid #ddd;
  padding: 0 3px;
}

.toolsbar-item {
  padding: 1px 5px 2px 5px;
  font-size: 18px;
  cursor: pointer;
  border-radius: 3px;
}
.toolsbar-item:hover {
  background: #f5f5f5;
}

.toolsbar-item-caret {
  font-size: 10px;
  padding-bottom: 5px;
}
</style>

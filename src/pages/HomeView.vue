<template>
  <my-context-menu text="SomeText" />
  <header-widget />
  <tools-bar @contextmenu.prevent />
  <a-row type="flex" class="content" @contextmenu.prevent="contextMenu">
    <a-col flex="250px">
      <left-bar />
    </a-col>
    <a-col flex="auto">
      <field-widget />
    </a-col>
    <a-col flex="250px">
      <right-bar />
    </a-col>
  </a-row>
</template>
<script>
import HeaderWidget from "@/components/HeaderWidget/HeaderWidget";
import ToolsBar from "@/components/ToolsBar/ToolsBar";
import LeftBar from "@/components/LeftBar/LeftBar";
import RightBar from "@/components/RightBar/RightBar";
import FieldWidget from "@/components/FieldWidget/FieldWidget";
import MyContextMenu from "@/components/UI/MyContextMenu/MyContextMenu";

export default {
  name: "HomeView",
  components: {
    HeaderWidget,
    ToolsBar,
    LeftBar,
    RightBar,
    FieldWidget,
    MyContextMenu,
  },
  data() {
    return {};
  },
  methods: {
    contextMenu(e) {
      let contextMenu = document.getElementsByClassName("contextMenu")[0];
      contextMenu.style.left = e.clientX + "px";
      contextMenu.style.top = e.clientY + "px";
      contextMenu.style.display = "block";
      console.log("showContextMenu!");
    },
  },
};
</script>

<style>
.content {
  height: calc(100vh - 60px - 40px);
}
</style>

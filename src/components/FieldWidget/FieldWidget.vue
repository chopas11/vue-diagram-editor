<template>
  <div class="field">
    <div
      @mousedown="itemEvent"
      @mouseup="upp"
      @click="clicck"
      id="field-item"
    ></div>
  </div>
</template>

<script>
import { RocketFilled } from "@ant-design/icons-vue";
import MyContextMenu from "@/components/UI/MyContextMenu/MyContextMenu";
// let block = document.getElementById("field-item");
export default {
  name: "FieldWidget",
  components: {
    // RocketFilled,
    // MyContextMenu,
  },
  methods: {
    itemEvent(e) {
      e.target.style.border = "1px dashed #41b883";
      function moveAt(e) {
        let block = document.getElementById("field-item");
        let coordsX = e.clientX - 250 - block.offsetWidth / 2;
        let coordsY = e.clientY - 100 - block.offsetHeight / 2;
        if (coordsX % 10 === 0) block.style.left = coordsX + "px";
        if (coordsY % 10 === 0) block.style.top = coordsY + "px";
      }
      document.onmousemove = function (e) {
        moveAt(e);
      };
      // e.target.style.position = "absolute";
    },
    upp(e) {
      e.target.style.border = "0";
      document.onmousemove = null;
    },
    clicck(e) {
      e.target.style.border = "1px dashed #41b883";
    },
  },
};
</script>

<style scoped>
.field {
  overflow-y: scroll;
  height: 100%;
  background: #f5f5f5;
}

#field-item {
  display: inline-block;
  position: relative;
  height: 100px;
  width: 100px;
  background: #ffffff;
  cursor: pointer;
}

/*#field-item::before {*/
/*  content: "100, 100";*/
/*  padding: 3px 5px;*/
/*  border-radius: 3px;*/
/*  height: 5px;*/
/*  position: relative;*/
/*  margin-left: auto;*/
/*  margin-right: auto;*/
/*  background: #ffffff;*/
/*}*/

/*#field-item:hover {*/
/*  border: 1px dashed #41b883;*/
/*}*/

/**/
.field::-webkit-scrollbar {
  width: 7px;
}
.field::-webkit-scrollbar-thumb {
  background-color: #555555;
  border-radius: 10px;
}
.field::-webkit-scrollbar-track {
}
</style>

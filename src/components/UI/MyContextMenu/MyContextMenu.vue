<template>
  <div class="contextMenu" id="wind">
    <ul>
      <li @click="undo">Undo <span>Ctrl + Z</span></li>
      <li>Clear the default style <span>Ctrl + Shift + A</span></li>
      <li>Select Edges <span>Ctrl + Shift + R</span></li>
      <li>Select all <span>Ctrl + A</span></li>
      <li>Undo <span>Ctrl + Z</span></li>
      <li>Clear the default style <span>Ctrl + Shift + A</span></li>
      <li>Select Edges <span>Ctrl + Shift + R</span></li>
      <li>Select all <span>Ctrl + A</span></li>
      <li>{{ text }} <span>Ctrl + A</span></li>
    </ul>
  </div>
</template>

<script>
export default {
  // let optionsObj = [
  //     {name: "Undo", shortcut: "Ctrl + Z", childs: [
  //       {name: "Child1", shortcut: "Ctrl + Z", childs: []},
  //       {name: "Child2", shortcut: "Ctrl + Z", childs: []},
  //       {name: "Child3", shortcut: "Ctrl + Z", childs: []},
  //     ]},
  //     {name: "Undo", shortcut: "Ctrl + Z", childs: []},
  //     ];
  name: "MyContextMenu",
  props: {
    text: {
      type: String,
    },
  },
  methods: {
    undo() {
      alert("Undo");
    },
  },
};
</script>

<style scoped>
.contextMenu {
  background: #ffffff;
  position: absolute;
  display: none;
  width: 300px;
  padding: 4px;
  top: 0;
  left: 0;
  border-radius: 3px;
  box-shadow: rgba(0, 0, 0, 0.16) 0px 1px 4px;
  z-index: 999;
}
.contextMenu ul {
  list-style: none;
  cursor: pointer;
  margin: 0;
}
.contextMenu ul li {
  padding: 5px 10px;
}
.contextMenu ul li span {
  float: right;
  font-size: 12px;
}
.contextMenu ul li:hover {
  background: #41b883;
  border-radius: 3px;
}
</style>

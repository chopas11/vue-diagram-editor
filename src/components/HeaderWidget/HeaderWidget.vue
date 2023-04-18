<template>
  <div class="header">
    <div class="header-image">
      <img src="../../assets/logo.png" alt="Logo" />
    </div>
    <div class="header-side">
      <span class="header-side-title">Untitled document</span>
      <ul>
        <li @click.stop="showOptions">File</li>
        <li @click.stop="showOptions">Edit</li>
        <li @click.stop="showOptions">View</li>
        <li @click.stop="showOptions">Options</li>
        <li @click.stop="showOptions">About</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "HeaderWidget",
  methods: {
    showOptions(e) {
      let contextMenu = document.getElementsByClassName("contextMenu")[0];
      contextMenu.style.left = e.target.getBoundingClientRect().x + "px";
      contextMenu.style.top = e.target.getBoundingClientRect().bottom + "px";
      contextMenu.style.display = "block";
      console.log("showOptions!");
    },
  },
};
</script>

<style scoped>
.header {
  background: #ffffff;
  padding: 8px 0 0 0;
  /*height: 60px;*/
  border-bottom: 1px solid #e6e6e6;
}

.header-image {
  display: inline-block;
  padding-left: 10px;
}

.header-image img {
  height: 40px;
  vertical-align: bottom;
  margin-bottom: 5px;
}

.header-side {
  display: inline-block;
  padding-left: 5px;
}

.header-side-title {
  font-size: 18px;
  padding: 1px 10px;
  border: 0;
  border-radius: 3px;
  cursor: text;
}
.header-side-title:hover {
  background: #f5f5f5;
}

.header-side ul {
  list-style: none;
  margin: 0;
  height: 25px;
}
.header-side ul li {
  list-style: none;
  display: inline;
  padding: 3px 10px;
  cursor: pointer;
  border-radius: 3px;
}
.header-side ul li:hover {
  background: #f5f5f5;
}
</style>

<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <VueTree :tree-data="treeData2" :tree-click-event="treeClickEvent"></VueTree>
  </div>
</template>

<script>
import VueTree from "./components/vue-tree.vue";

export default {
  name: 'App',
  components: {
    VueTree
  },
  data () {
    return {
      treeData2: [
        {
          text: "一级", // 显示的文字
          expand: false, // 默认是否展开
          children: [
            {
              text: "二级-1",
              expand: false,
            },
            {
              text: "二级-2",
              expand: false,
              children: [
                {
                  text: "三级-1",
                  expand: false,
                },
                {
                  text: "三级-2",
                  expand: false,
                  children: [
                    {
                      text: "四级-1",
                      expand: false,
                    }
                  ]
                }
              ]
            }
          ]
        },
        {
          text: "一级-2",
          expand: false
        }
      ]
    }
  },
  methods: {
    treeClickEvent(item){
      console.log(item);
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

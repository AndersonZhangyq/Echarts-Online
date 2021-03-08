<template>
  <q-page>
    <div
      id="luckysheet"
      style="position: absolute;width: 100%;left: 0px;top: 0px;bottom: 0px;right: 0px"
    ></div>
  </q-page>
</template>

<script>
export default {
  name: "Data",
  data() {
    return {
      leftDrawerOpen: false
    };
  },
  mounted() {
    // In some cases, you need to use $nextTick
    // this.$nextTick(() => {
    luckysheet.create({
      container: "luckysheet", // 设定DOM容器的id
      title: "Luckysheet Demo", // 设定表格名称
      lang: "zh", // 设定表格语言
      plugins: ["chart"],
      showtoolbar: false,
      showtoolbarConfig: {
        undoRedo: true,
        paintFormat: true, //格式刷
        numberDecrease: true, // '减少小数位数'
        numberIncrease: true, // '增加小数位数
        font: true, // '字体'
        fontSize: true, // '字号大小'
        bold: true, // '粗体 (Ctrl+B)'
        italic: true // '斜体 (Ctrl+I)'
      }
    });

    // });
  }
};
</script>

<template>
  <section>
    <banner></banner>
    <TabIndication></TabIndication>
  </section>
</template>

<script>
import banner from "./banner";
import TabIndication from "./TabIndication";

export default {
  name: "IndexDemo",
  components: {
    banner,
    TabIndication
  }
}
</script>

<style>
.el-tabs__nav {
  /*border: 1px solid red;*/
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
.el-tabs__item{
  /*border: 1px solid red ;*/
  margin: 0 100px;
  font-weight: bold;
  font-size: 16px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
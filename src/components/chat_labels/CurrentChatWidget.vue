<template>
  <div class="label">
    <div class="panel chat"></div>
    <div class="panel users"></div>
  </div>
</template>

<script>
export default {
  name: "CurrentChatWidget"
}
</script>

<style scoped>
.label{
  margin: 8px;
  width: calc(100% - 16px);
  height: calc(100% - 16px);
  background-color: teal;
}
.panel{
  display: inline-block;
  height: 100%;
}
.panel.users{
  float: right;
  width: 300px;
  background-color: #002480;
}
.panel.chat{
  width: calc(100% - 308px);
  background-color: rgb(255, 255, 255);
}
</style>
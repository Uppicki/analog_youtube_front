<template>
  <my-header class="h"/>
  <div class="content">
    <chat-widget/>
  </div>
</template>

<script>
import myHeader from "@/components/MyHeader";

import chatWidget from "@/components/ChatWidget";


export default {
  name: 'App',
  components: {
    myHeader,
    chatWidget
  }
}
</script>

<style>
.h{
  z-index: 5;
  min-width: 800px;
}
.content{
  top: 76px;
  position: absolute;
  margin: -8px;
  padding: 8px;

  width: calc(100% - 16px);
  height: calc(100% - 84px);
  background-color: black;
  min-height: 400px;
  min-width: 800px;
}
</style>

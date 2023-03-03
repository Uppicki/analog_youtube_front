<template>
  <div class="left-menu">asd</div>
  <div class="chat-label">
    <create-chat-widget v-if="widget === 'new'"/>
    <find-chat-widget v-if="widget === 'find'"/>
    <current-chat-widget v-if="widget === 'chat'"/>
  </div>
</template>

<script>
import CreateChatWidget from "@/components/chat_labels/CreateChatWidget";
import FindChatWidget from "@/components/chat_labels/FindChatWidget";
import CurrentChatWidget from "@/components/chat_labels/CurrentChatWidget";
export default {
  name: "ChatWidget",
  components: {CurrentChatWidget, FindChatWidget, CreateChatWidget},
  data() {
    return {
      widget: "chat"

    }
  }
}
</script>

<style scoped>
.left-menu{
  display: inline-block;
  width: 300px;
  height: 100%;
  background-color: #db1b1b;
}
.chat-label{
  margin: -8px;
  float: right;
  display: inline-block;
  width: calc(100% - 300px);
  height: calc(100% + 16px);
  background-color: #db1b1b;
}
</style>
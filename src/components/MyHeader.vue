<template>
  <div class="my-header">
    <div class="img-menu-btn">asd</div>
    <div class="nav-links">
      <a class="nav-link">Видео</a>
      <a class="nav-link">Чат</a>
    </div>

    <div @mouseover="userTabVisible = true"
         @mouseleave="userTabVisible = false"
         class="user-tab">
      <div class="user-img"></div>
      <transition name="user-name">
        <div v-if="userTabVisible"
             class="user-tab-name">aa</div>
      </transition>

    </div>


  </div>
</template>

<script>
export default {
  name: "MyHeader",
  data() {
    return {
      userTabVisible: false

    }
  }
}
</script>

<style scoped>
.my-header{
  position: absolute;
  margin: -8px;
  width: 100%;
  height: 60px;
  background-color: #2c3e50;
}

.img-menu-btn{
  display: inline-block;
  margin-top: 8px;
  margin-left: 20px;
  width: 40px;
  height: 40px;
  background-color: white;
}
.img-menu-btn:hover{
  background-color: black;
}

.nav-links{
  margin-left: 50px;
  width: 300px;
  display: inline-block;
}

.nav-link{

  height: 40px;
  display: inline-block;
  margin-top: 8px;
  margin-left: 20px;
  background-color: white;
}
.nav-link:hover{
  background-color: black;
}

.user-tab{
  margin-right: 20px;
  margin-top: 8px;
  float: right;
  display: inline-block;
  height: 40px;
  background-color: white;
}



.user-img{
  margin: 2px;
  float: right;
  display: inline-block;
  height: 36px;
  width: 36px;
  background-color: rgb(54, 53, 53);
}

.user-tab-name{
  transition-delay: 0.5s;
  display: inline-block;
  width: 100px;
  background-color: #db1b1b;
}




.user-name-enter-active, .user-name-leave-active {
  display: inline-block;
  width: 100px;
  transition: opacity 0.5s ease;
}
.user-name-enter-from, .user-name-leave-to{
  display: inline-block;
  opacity: 0;
}

</style>
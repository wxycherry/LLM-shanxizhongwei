<script setup lang="ts">
import { ref } from "vue";
import { useRouter } from "vue-router";
import { useChatStore } from "@/stores/chat";
import Login from "./components/Login.vue";
import Register from "./components/Register.vue";

const chatStore = useChatStore();
const router = useRouter();

const status = ref<"login" | "register">("login");
</script>
<template>
  <div class="flex h-full w-full bg-blue justify-between items-center bg-blue-500">
    <div class="h-full w-1/2 flex items-center justify-center">
      <img src="../../assets/image/login/login_pic.png" class="w-[500px] h-[400px]">
    </div>
    <div class="h-full w-1/2 flex items-center justify-center bg-white rounded-l-[40px]">
      <div 
        class="flex flex-col items-center h-[450px] w-3/5 justify-between">
        <!-- <img src="../../assets/login_title.png" class="w-full mb-8"> -->
         <div class="content">
          <img src="../../assets/图片2.png" alt="">
         <p>网络安全私域大模型</p
          ></div>
         
        <Login 
          v-if="status === 'login'" 
          v-model:status="status" />
        <Register
          v-else-if="status === 'register'"
          v-model:status="status" />
      </div>
    </div>
  </div>
</template>
<style scoped>
.content{
  display: flex;
  justify-content: center;
  align-items: center;
}
.content p{
  color: rgb(86, 150, 247);
  font-size: 40px;
  font-weight: bold;
  font-family: KaiTi;
}
</style>

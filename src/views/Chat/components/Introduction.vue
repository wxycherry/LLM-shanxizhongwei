<script setup lang="ts">
import { useChatStore } from "@/stores/chat";
const chatStore = useChatStore();
import { useRouter } from "vue-router";
const router = useRouter();
import HotWords from "./HotWords.vue";
import Input from "./Input.vue";

const sendQuestion = (question: string) => {
  console.log(555);
  router.push({
    path: "/chat",
  });
  //   chatStore.setQuestion(question)
  //   chatStore.setMode(mode.value)
  //   chatStore.setShowResult(true)
};
</script>
<template>
  <div class="mx-auto w-11/12 md:w-1/2">
    <div
      class="bg-[url(/src/assets/image/introduction/bg_introduction.png)] bg-cover bg-center rounded-xl bg-no-repeat w-full h-[330px] mx-auto mt-24 overflow-hidden"
    >
      <div
        class="bg-gradient-to-r from-[#1e3b8ae0] to-[#0285c7e0] w-full h-full text-white flex flex-col justify-between p-6"
      >
        <h2 class="text-xl font-normal tracking-wide">
          Hi,我是您的网络安全私域大模型智能助手，我可以回答任何网络安全相关的问题。
        </h2>
        <ul class="text-sm ml-4">
          <li class="list-disc py-4">网络安全的基本概念是什么？</li>
          <li class="list-disc py-4">常见的网络安全威胁有哪些？</li>
          <li class="list-disc py-4">如何保护个人数据免受网络攻击？</li>
        </ul>
        <div class="pt-4 text-xs">
          <button class="px-3 py-2 rounded-xl mr-4 border border-white">
            网络安全漏洞扫描
          </button>
          <button class="px-3 py-2 rounded-xl mr-4 border border-white">
            网络入侵检测分析
          </button>
          <button class="px-3 py-2 rounded-xl mr-4 border border-white">
            安全合规报告生成
          </button>
        </div>
      </div>
    </div>
    <HotWords class="mt-1" />
  </div>
  <!-- <Input @sendQuestion = "sendQuestion"/> -->
</template>

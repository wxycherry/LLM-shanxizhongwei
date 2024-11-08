<script setup lang="ts">
import { ref } from "vue"
const words = ref(['网络安全', '防火墙', '加密技术', '入侵检测', '数据保护'])
</script>
<template>
 <div class="text-gray-700 text-xs lg:text-sm">
    <span>热词：</span>
    <span 
        v-for="item in words" :key="item" class="mr-2">
        {{ item }}
    </span>
</div>   
</template>
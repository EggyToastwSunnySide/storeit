<script setup lang="ts">
// Mã tự sinh (tag tài sản DSK-0022, mã phiếu REQ-0004, mã loại DESK): một kiểu ở mọi nơi, chữ
// mono màu liên kết như mã tag của bản cũ; trong liên kết thì lấy màu liên kết
defineProps<{ code: string }>()
</script>

<template>
  <span class="code-tag">{{ code }}</span>
</template>

<style scoped>
.code-tag {
  font: 0.92em var(--app-mono);
  white-space: nowrap;
}
a .code-tag {
  color: var(--app-link);
}
</style>

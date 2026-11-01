<script setup lang="ts">
// Logo StoreIt: ô xanh một màu bo góc, bên trong bốn thanh xoay vòng quanh một ô
// vuông (bốn kệ của kho bao lấy một món đồ; vòng xoay là mượn đi, trả về). Một hình hình học, một
// màu, nhận ra được ở 16px (favicon.svg cùng hình). markOnly: chỉ ô biểu tượng, không có chữ
defineProps<{ markOnly?: boolean }>()
</script>

<template>
  <span class="app-logo">
    <svg class="mark" viewBox="0 0 32 32" aria-hidden="true">
      <rect width="32" height="32" rx="8.5" fill="#059669" />
      <g fill="#fff">
        <rect x="7" y="7" width="12.4" height="5" rx="1.3" />
        <rect x="20" y="7" width="5" height="12.4" rx="1.3" />
        <rect x="12.6" y="20" width="12.4" height="5" rx="1.3" />
        <rect x="7" y="12.6" width="5" height="12.4" rx="1.3" />
        <rect x="13.4" y="13.4" width="5.2" height="5.2" rx="1.2" fill-opacity="0.5" />
      </g>
    </svg>
    <span v-if="!markOnly" class="word">StoreIt</span>
  </span>
</template>

<style scoped>
.app-logo {
  display: inline-flex;
  align-items: center;
  gap: 0.6em;
  font: 700 1.35rem var(--app-display);
  letter-spacing: -0.035em;
  line-height: 1;
}
.mark {
  width: 1.6em;
  height: 1.6em;
  flex: none;
}
</style>

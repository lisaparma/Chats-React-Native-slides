<template>
  <div class="slide-number">
    {{ $slidev.nav.currentPage }} / {{ $slidev.nav.total }}
  </div>
</template>

<style scoped>
.slide-number {
  position: fixed;
  bottom: 14px;
  right: 16px;
  font-family: 'DM Mono', monospace;
  font-size: 0.72em;
  color: rgba(148, 163, 184, 0.6);
  z-index: 200;
  pointer-events: none;
}
</style>

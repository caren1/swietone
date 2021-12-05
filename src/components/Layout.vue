<template>
  <div class="layout">
    <slot />
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "@/assets/_variables.scss";

.layout {
  height: 100%;
  background-color: $champion-green;
}
</style>

<script setup>
const props = defineProps({ disabled: { type: Boolean, default: false } })
</script>

<template>
  <button class="cs-button" :disabled="disabled"><span class="cs-button__text">
      <slot />
    </span></button>
</template>

<style scoped>
.cs-button {
  width: 335px;
  background: var(--button-primary);
  color: var(--button-default-text);
  border-radius: 100px;
  padding: 16px 10px 16px 10px;
  border: none;
  cursor: pointer;
}

.cs-button__text {
  font-size: 24px;
  line-height: 36px;
  font-weight: 400;
}

.cs-button:disabled {
  cursor: not-allowed;
  background: var(--button-disabled-bg);
  color: var(--button-disabled-text);
}
</style>
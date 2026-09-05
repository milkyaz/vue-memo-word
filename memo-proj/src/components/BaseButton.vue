<script setup>
const props = defineProps(
  { disabled: { type: Boolean, default: false } },
)
</script>

<template>
  <button class="cs-button" :disabled="disabled"><span class="cs-button__text">
      <slot />
    </span></button>
</template>

<style scoped>
.cs-button {
  background: var(--button-primary);
  color: var(--button-default-text);
  font-family: inherit;
  border-radius: 100px;
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
<script setup></script>

<template>
  <button>
    <slot name="button">Войти</slot>
  </button>
</template>

<style scoped>
button {
  width: 100%;
  height: 42px;
  border-radius: 4px;
  padding: 8px;
  background-color: #373653;
  color: white;
  font-size: 14px;
  /* font-family: Onest; */
  font-weight: 700;
}
</style>

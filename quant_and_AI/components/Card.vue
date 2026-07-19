<script setup lang="ts">
defineProps<{ title?: string }>()
</script>

<template>
  <div class="card">
    <b v-if="title || $slots.title"><slot name="title">{{ title }}</slot></b>
    <hr class="my-2" />
    <slot />
  </div>
</template>

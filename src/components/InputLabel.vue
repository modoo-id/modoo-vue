<script setup>
defineProps({
  value: String,
  required: {type: Boolean, default: false},
});
</script>

<template>
  <label class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">
    <span v-if="value">
      {{ value }}
      <span
        v-if="required"
        class="text-red-500 ms-1"
      >
        (*)
      </span>
    </span>
    <span v-else>
      <slot />
      <span
        v-if="required"
        class="text-red-500 ms-1"
      >
        (*)
      </span>
    </span>
  </label>
</template>

<script setup>
import {Link} from "@inertiajs/vue3";

defineProps({
  href: {
    type: String,
  },
});
</script>

<template>
  <Link
    :href="href"
    class="text-gray-800 dark:text-white hover:bg-gray-50 focus:ring-4 focus:ring-gray-300 font-medium rounded-lg text-sm px-4 lg:px-5 py-2 lg:py-2.5 mr-2 dark:hover:bg-gray-700 focus:outline-none dark:focus:ring-gray-800"
  >
    <slot />
  </Link>
</template>

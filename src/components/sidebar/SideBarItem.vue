<template>
  <li
    :class="[
      'flex items-center font-medium  transition-all rounded-r-full cursor-pointer',
      active === item.title ? 'bg-orange-active' : 'hover:bg-base-200',
    ]"
  >
    <span v-html="item.icon" class="py-3 px-8"></span>
    <span>{{ item.title }}</span>
  </li>
</template>

<script setup>
defineProps({
  item: {
    type: Object,
    required: true,
  },
  active: {
    type: String,
    required: true,
  },
})
</script>

<style scoped></style>

<template>
  <div class="w-64 h-full mt-1">
    <ul>
      <template v-for="list in lists" :key="list.id">
        <SideBarItem
          :item="list"
          :active="active"
          @click="active = list.title"
        />
      </template>
    </ul>
  </div>
</template>

<script setup>
import SideBarItem from './SideBarItem.vue'
import lists from '../../public/SideBarItemList'

import { ref } from 'vue'
const active = ref('Notes')
</script>

<style scoped></style>

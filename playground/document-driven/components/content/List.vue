<script setup lang="ts">
import { useUnwrap } from '#imports'
// Utils from Nuxt Content
const { flatUnwrap } = useUnwrap()

</script>

<template>
  <ul>
    <li v-for="(item, index) of flatUnwrap($slots.default!(), ['ul'])" :key="index">
      ☑︎
      <span><ContentSlot :use="() => item" unwrap="li" /></span>
    </li>
  </ul>
</template>

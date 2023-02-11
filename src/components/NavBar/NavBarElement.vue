<script setup lang="ts">
// eslint-disable-next-line @typescript-eslint/no-unused-vars
const props = defineProps(["linkHref", "isActive"]);
</script>

<template>
  <li class="nav-item">
    <RouterLink
      class="nav-link"
      :class="isActive == 'true' ? 'active' : ''"
      :to="props.linkHref"
      ><slot></slot
    ></RouterLink>
  </li>
</template>

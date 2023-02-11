<script setup lang="ts">
import SQLForm from "../components/SQLForm.vue";
import CodeBlock from "@/components/CodeBlock.vue";

import { ref } from "vue";

let formData = ref("");

const returnData = (data: string) => {
  formData.value = data;
};
</script>

<template>
  <main>
    <SQLForm @return-data="returnData"></SQLForm>
    <CodeBlock>{{ formData }}</CodeBlock>
  </main>
</template>

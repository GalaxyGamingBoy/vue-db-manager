<script setup lang="ts">
import { ref } from "vue";

const emit = defineEmits(["returnData"]);

const mysqlUrl = ref("");
const sql = ref("");

const sendGET = () => {
  return "{}";
};

const formSubmit = () => {
  emit("returnData", sendGET());
};
</script>

<template>
  <div class="m-3">
    <!-- MySQL URL -->
    <div class="input-group mb-3">
      <span class="input-group-text" id="mysql-url">MySQL URL:</span>
      <input
        type="password"
        class="form-control"
        placeholder="mysql://"
        aria-label="MySQL URL"
        aria-describedby="mysql-url"
        v-model="mysqlUrl"
      />
    </div>

    <!-- SQL -->
    <div class="input-group mb-3">
      <span class="input-group-text" id="sql">SQL:</span>
      <input
        type="text"
        class="form-control"
        placeholder="SELECT *"
        aria-label="SQL"
        aria-describedby="sql"
        v-model="sql"
      />
    </div>

    <!-- Submit -->
    <button type="submit" class="btn btn-primary" @click="formSubmit">
      Send!
    </button>
  </div>
</template>

<script setup lang="ts">
import NavBarElement from "./NavBar/NavBarElement.vue";
const props = defineProps(["name"]);
</script>

<template>
  <nav class="navbar navbar-expand-lg bg-body-tertiary">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">{{ props.name }}</a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
          <NavBarElement link-href="/" is-active="true">Home</NavBarElement>
          <NavBarElement link-href="/about">About</NavBarElement>
          <NavBarElement link-href="/SQLTemplates">SQL Templates</NavBarElement>
        </ul>
      </div>
    </div>
  </nav>
</template>

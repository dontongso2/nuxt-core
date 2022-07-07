<template>
  <div class="layout-default">
    <LayoutHeader></LayoutHeader>

    <h1>abc</h1>

    <nuxt />
  </div>
</template>

<script>
import LayoutHeader from "@/components/Layout/Header.vue";

export default {
  name: "default",

  components: {
    LayoutHeader,
  },
};
</script>

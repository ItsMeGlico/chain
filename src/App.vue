<script setup>
import HomeView from "@/views/HomeView.vue";
import KaKaoMap from "./components/KakaoMap.vue";

export default {
  name: "App",
  components: {
    KakaoMap,
  },
};
</script>

<template>
  <HomeView />
</template>

<style scoped></style>

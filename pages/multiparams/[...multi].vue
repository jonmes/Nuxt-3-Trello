<template>
  <div>
    <h1>{{ params }}</h1>
  </div>
      <button
      @click="
        setColorTheme($colorMode.preference === 'dark' ? 'light' : 'dark')
      "
    >
      Toogle DarkMode
    </button>
</template>

<script setup>
const route = useRoute();

const params = ref(route.params.multi);
</script>

<style lang="scss" scoped></style>

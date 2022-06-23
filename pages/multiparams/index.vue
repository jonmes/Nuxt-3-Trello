<template>
  <div class="min-h-screen bg-green-100 dark:bg-gray-700">
    <h1 class="text-7xl">MultiParams Index Page.</h1>
    <h2 class="text-7xl">Hello</h2>
    <button
      class="bg-green-400 px-4 py-2 rounded-lg"
      @click="
        setColorTheme($colorMode.preference === 'dark' ? 'light' : 'dark')
      "
    >
      Toogle DarkMode
    </button>
  </div>
</template>

<script setup>
const setColorTheme = inject("setColorTheme");
</script>

<style lang="scss" scoped></style>

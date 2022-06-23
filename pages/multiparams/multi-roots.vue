<template>
  <div class="min-h-screen bg-green-100 dark:bg-gray-700">
    <h1 class="text-black dark:text-white">Multi root</h1>
    <h2 class="text-black dark:text-white">multi root</h2>
    <a class="text-black dark:text-white" href="/multiparams"
      >back to multiParams</a
    >
    <br />
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

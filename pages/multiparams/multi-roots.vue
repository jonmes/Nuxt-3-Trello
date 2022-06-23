<template>
  <div class="bg-green-100 dark:bg-gray-700">
    <h1 class="text-black dark:text-white">Multi root</h1>
    <h2 class="text-black dark:text-white">multi root</h2>
    <a class="text-black dark:text-white" href="/multiparams"
      >back to multiParams</a
    >

    <button
      @click="
        setColorTheme($colorMode.preference === 'dark' ? 'light' : 'dark')
      "
    >
      Toogle DarkMode
    </button>
  </div>
</template>

<script setup>
const setColorTheme = inject(setColorTheme);
</script>

<style lang="scss" scoped></style>

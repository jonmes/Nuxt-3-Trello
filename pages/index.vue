<script setup>
const setColorTheme = inject("setColorTheme");
</script>
<template>
  <div class="min-h-screen bg-green-100 dark:bg-gray-700">
    <h1 class="dark:text-white text-black text-8xl">Hello</h1>
    <a href="/multiparams">Go To MulitiParams</a>
    <br />
    <button
      class="bg-green-400 px-4 py-2 rounded-3xl"
      @click="
        setColorTheme($colorMode.preference === 'dark' ? 'light' : 'dark')
      "
    >
      Toogle DarkMode
    </button>
  </div>
</template>

<style lang="scss" scoped></style>

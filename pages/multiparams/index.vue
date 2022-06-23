<template>
  <div class="min-h-screen bg-green-100 dark:bg-gray-700 text-7xl">
    <h1>MultiParams Index Page.</h1>
    <h2>Hello</h2>
        <button
      @click="
        setColorTheme($colorMode.preference === 'dark' ? 'light' : 'dark')
      "
    >
      Toogle DarkMode
    </button>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped></style>

<template>
  <div>
    <NuxtLayout name="landing">
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>

<script setup>
const setColorTheme = (newTheme) => {
  useColorMode().preference = newTheme;
};

provide("setColorTheme", setColorTheme);
</script>

<style lang="scss" scoped></style>

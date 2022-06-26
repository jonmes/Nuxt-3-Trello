<template>
  <suspense>
    <template #default>
      <div
        v-if="waiter"
        class="min-h-screen bg-green-100 duration-500 dark:bg-slate-700"
      >
        <div class="text-black dark:text-white duration-500">
          <h1>{{ params }}</h1>
        </div>
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
    <template #fallback>
      <div class="min-h-screen bg-blue-600">
        <h1 class="text-2xl">Wait a moment man please</h1>
      </div>
    </template>
  </suspense>
</template>

<script setup>
const route = useRoute();
const params = ref(route.params.multi);
const setColorTheme = inject("setColorTheme");

const waiter = ref(false);

setTimeout(() => {
  waiter.value = true;
}, 5000);
</script>

<style lang="scss" scoped></style>

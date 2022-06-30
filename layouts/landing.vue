<template>
  <div @scroll="handleScroll">
    <Navbar />
    <slot />
  </div>
</template>

<script setup>
onMounted(() => window.addEventListener("scroll", handleScroll));

const handleScroll = () => {
  console.log("helo scroll");
};

// const scrollClass = ref("");

// const scrollFunc = () => {
//   scrollClass.value = "shadow-none hover:shadow-opaq duration-300";
//   console.log('hello');
// };
</script>

<style scoped></style>

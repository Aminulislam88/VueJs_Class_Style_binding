<script setup>

const items=[1,2,3,4,,5,6]
</script>

<template>
  <body class="p-10">
    <section class="mx-auto container flex items-center text-center flex-col space-y-2">
        <div class="p-5 border border-gray-600 w-40" v-for="item in items">{{ item }}</div>
    </section>
</body>
</template>

<style scoped>

</style>

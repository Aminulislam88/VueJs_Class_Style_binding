<script setup>

const tasks=[
    "complete project proposel",
    "Update website content",
    "Fix bug in user authentication",
    "prepare Presentation Slide",
    "Software update"
]
</script>

<template>
  <body class="p-10">
    <section class="mx-auto container flex items-center text-center flex-col space-y-2">
        <div class="p-5 border border-gray-600 w-40" v-for="(task,index) in tasks">{{index +1}}-{{ task }}</div>
    </section>
</body>
</template>

<style scoped>

</style>

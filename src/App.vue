<script setup>
const bgOrange="bg-orange-400"
const bgIndigo="bg-indigo-400"
const bgGreen="bg-green-400"

//const bgRed="bg-red-600"
const weekday=false

const colors={
    bgTeal:"bg-teal-100",
    borderTeal:"border-teal-500",
    textTeal:"text-teal-900"
}
const messeageType="warning"
if('error'==messeageType){
  colors.bgTeal="bg-red-100"
  colors.borderTeal="border-red-500",
    colors.textTeal="text-red-900"
}
if('warning'==messeageType){
  colors.bgTeal="bg-orange-100"
  colors.borderTeal="border-orange-500",
    colors.textTeal="text-orange-900"
}

</script>

<template>
   <section class="container mx-auto">
        <h1 class="text-center text-2xl py-10">Class & Style Binding</h1>

        <section class="flex space-x-10">
            <div class="w-1/3 h-16" :class="bgOrange"></div>
            <div class="w-1/3 h-16" :class="bgIndigo"></div>
            <div class="w-1/3 h-16" :class="bgGreen"></div>
        </section>

        <section class="mt-10">
            <div class="h-16 flex items-center justify-center text-white" :class="weekday?'bg-green-400':'bg-indigo-400'">
                It's a weekday!
            </div>
        </section>

        <section class="mt-10">
            <div class=" border-t-4  rounded-b  px-4 py-3 shadow-md" :class=[colors.bgTeal,colors.borderTeal,colors.textTeal] >
                <p class="font-bold">Our privacy policy has changed</p>
                <p class="text-sm">Make sure you know how these changes affect you.</p>
            </div>
        </section>
    </section>
</template>

<style scoped>

</style>

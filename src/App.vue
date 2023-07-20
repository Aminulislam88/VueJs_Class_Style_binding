<script setup>

const tasks=[ 
   {id:1, title:"complete project proposel",status:"Completed"},
   {id:2,title:"Update website content",status:"In Progress"},
   {id:3,title:"Fix bug in user authentication",status:"Completed"},
   {id:4,title:"prepare Presentation Slide",status:"In Progress"},
   {id:5,title:"Software update",status:"Completed"}
];

function getCompleteStatus(){
    return tasks.filter(task=>"Completed"==task.status)
}

function getInprogressStatus(){
    return tasks.filter(task=>"In Progress"==task.status)
}

const persons={
    name:"Aminul",
    age:"23",
    email:"aminul@gmail.com"
}
</script>

<template>
  <body class="p-10">
    <section class="mx-auto container flex items-center text-center flex-col space-y-2">
        <!-- <div class="p-5 border border-gray-600 w-40" v-for="task in tasks" :key="task.id">{{task.id}}-{{ task.title }}</div> -->
        <!-- <div class="p-5 border border-gray-600 w-40" v-for="(task,index) in tasks" :key="index">{{task.id}}-{{ task.title }}</div> -->
        <h2>Completed Status</h2>
         <div class="p-5 border border-gray-600 w-40" v-for="(task,index) in tasks" v-show="task.status=='Completed'" :key="index">{{task.id}}-{{ task.title }}</div>
        <!-- <div class="p-5 border border-gray-600 w-40" v-for="task in getCompleteStatus()" :key="task.id">{{task.id}}-{{ task.title }}</div> -->
        <h2>In Progress Status</h2>
        <div class="p-5 border border-gray-600 w-40" v-for="task in getInprogressStatus()" :key="task.id">{{task.id}}-{{ task.title }}</div>
        <h2>object Loop</h2> 
         <div class="p-5 border border-gray-600 w-40" v-for="(value,key,index) in persons" :key="index">{{index+1}}-{{key}} : {{ value }}</div> 

    </section>
</body>
</template>

<style scoped>

</style>

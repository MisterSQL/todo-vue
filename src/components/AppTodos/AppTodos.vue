<template>
  <div class="container">
    <h1>Список задач</h1>
    <AppTodosList />
  </div>
</template>


<script>
  import AppTodosList from "@/components/AppTodos/AppTodosList.vue";

  export default {
    name:'AppTodos',
    components:{
      AppTodosList
    },
  }
</script>

<template>
  <div class="todos-list">
    <AppTodosItem />
  </div>
</template>

<script>
  import AppTodosItem from "@/components/AppTodos/AppTodosItem.vue";

  export default {
    name: 'AppTodoList',
    components: {
      AppTodosItem
    },
  }
</script>

<style scoped>
  .todos-list {
    display: grid;
    --cards : 3;
    grid-template-columns: repeat(var(--cards),minmax(300px,600px));
    margin-top: 53px;
    gap: 50px;
  }

  @media screen and (max-width: 1184px) {
    .todos-list {
      --cards: 2;
    }
  }

  @media screen and (max-width: 740px) {
    .todos-list {
      --cards: 1;
    }
  }
</style>

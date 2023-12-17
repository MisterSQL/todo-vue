<template>
<!--  TODO: убрать клик с модалки и модалку сделать иным образом, никих обращений через document....-->
  <div id="app" @click="closeModal($event)">
    <AppModal />
    <TheHeader />
    <AppTodos class="todos" />
  </div>
</template>

<script>
//TODO: rename components
import TheHeader from '@/components/TheHeader/TheHeader.vue'
import AppTodos from "@/components/AppTodos/AppTodos.vue";
import AppModal from "@/components/AppModal.vue";

export default {
  name: 'App',
  components: {
    AppModal,
    TheHeader,
    AppTodos,
  },
  methods: {
    closeModal(event) {
      const idModal = document.getElementById(modal.data().idName);
      const element = event.target;

      if(element.classList.contains('modal')) {
        idModal.classList.add('hidden');
      }
    }
  }
}
</script>

<style scoped>
.todos {
  margin-top: 54px;
}
</style>

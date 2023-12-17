<template>
  <header class="header">
    <div class="header__container container">
      <AppLogo />
      <AppButton
          class="header__button"
          label="Создать"
          @click="openModal()"
      />
    </div>
  </header>
</template>

<script>
  import AppButton from "@/components/ui/AppButton.vue";
  import AppLogo from "@/components/AppLogo.vue";
  import AppModal from "@/components/AppModal.vue";

  export default {
    components:{
      AppButton,
      AppLogo,
      AppModal,
    },
    methods: {
      openModal() {
        const idName = modal.data().idName;
        const modalWindow = document.getElementById(idName);
        modalWindow.classList.remove('hidden');
      }
    }

  }
</script>

<style scoped>
  @import "@/assets/style/variables.css";

  .header__button {
    border: 1px solid white;
    color: var(--color-primary);
    border-radius: 2px;
    height: 36px;
    padding-inline: 26px;
    text-transform: uppercase;
    transition: .4s;
  }

  .header__button:hover {
    background-color: var(--color-primary);
    color: var(--color-secondary);
  }

  .header {
    background-color: var(--color-secondary);
    width: 100%;
  }

  .header__container {
    display: flex;
    align-items: center;
    margin: 0 auto;
    justify-content: space-between;
    padding-block: 16px;
  }

  @media screen and (max-width: 1435px) {
    .container {
      --container-padding: 128px;
    }
  }

  @media screen and (max-width: 1024px) {
    .container {
      --container-padding: 64px;
    }
  }

  @media screen and (max-width: 740px) {
    .container {
      --container-padding: 16px;
    }
  }
</style>

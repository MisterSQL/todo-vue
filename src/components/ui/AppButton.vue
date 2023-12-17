<template>
  <button
      class="button"
      type="button"
      @click="$emit('click')"
  >
    {{ label }}
  </button>
</template>

<script>
export default {
  name:'AppButton',
  props: {
    label: {
      type: String,
      default: 'Кнопка',
    },
  },
}
</script>


<style scoped>
.button {
  background-color: transparent;
  color: var(--color-secondary);
  font-weight: 500;
}
</style>

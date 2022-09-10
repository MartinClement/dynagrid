<template>
  <div class="dg-grid">
    <slot />
  </div>
</template>

<script>
  export default {
    name: 'DGGrid',
  }
</script>

<style lang="postcss" scoped>
  .dg-grid {
    display: grid;
    grid-template-columns: repeat(20, 1fr);
    gap: 20px;
  }

  @media (max-width: 800px) {
    .dg-grid {
      grid-template-columns: repeat(10, 1fr);
      gap: 10px;
    }
  }
</style>
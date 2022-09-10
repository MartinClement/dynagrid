<template>
  <div class="dg-content-wrapper">
    <slot />
  </div>
</template>

<script>
  export default {
    name: 'DGContentWrapper',
  }
</script>

<style lang="postcss" scoped>
  .dg-content-wrapper {
    margin: auto;
    padding: 24px;
    max-width: 80%;
    background-color: #eee;
  }

  @media (max-width: 800px) {
    .dg-content-wrapper {
      max-width: 100%;
    }
  }
</style>
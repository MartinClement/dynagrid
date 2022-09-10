<template>
  <div class="dg-item">
    <img class="image" src="https://picsum.photos/800/400" alt="item image">
    <div class="desc">
      <div class="title">{{ title }}</div>
      <div class="text">{{ text }}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DGItem',
  props: {
    title: { type: String, default: '' },
    text: { type: String, default: ''},
  }
}
</script>

<style lang="postcss" scoped>
  .dg-item {
    border-radius: 8px;
    background-color: #fff;
    display: flex;
    flex-flow: column nowrap;
    gap: 10px;
    grid-column: span 5;
  }

  .image {
    border-radius: 8px;
  }

  .desc {
    padding: 8px 16px;
  }

  .title {
    font-size: 16px;
    font-weight: 700;
  }

  @media (max-width: 800px) {
    .dg-item {
      grid-column: span 5;
    }
  }
</style>
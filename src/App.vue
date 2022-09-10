<template>
  <div id="app">
    <DGContentWrapper>
      <DGGrid>
        <DGItem
          v-for="(item, ii) in items"
          :key="ii"
          :title="item.title"
          :text="item.text"
        />
      </DGGrid>
    </DGContentWrapper>
  </div>
</template>

<script>
import DGContentWrapper from './components/wrapper/DGContentWrapper.vue';
import DGGrid from './components/grid/DGGrid.vue';
import DGItem from './components/grid/DGItem.vue';

const getItems = nb  => Array(nb).fill(undefined).map((val, index) => {
  return { title: `Grid Item ${index}`, text: `Here you can see an item in the grid at the index: ${index}`};
});

export default {
  name: 'App',
  components: { DGContentWrapper, DGGrid, DGItem },
  computed: {
    items() {
      return getItems(20);
    }
  }
}
</script>

<style scoped lang="postcss">
  #app {
    padding: 30px 0;
  }
</style>

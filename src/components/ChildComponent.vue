<template>
  <div class="detail-rt">
    <h2>Detail RT (Rukun Tetangga)</h2>
    <nested-component @pejabat-selected="emitToParent">
      <slot name="defaultSlot"></slot>
    </nested-component>
  </div>
</template>

<script>
import NestedComponent from './NestedComponent.vue';

export default {
  components: {
    NestedComponent
  },
  methods: {
    emitToParent(data) {
      this.$emit('pejabat-selected', data);
    }
  }
};
</script>

<style scoped>
.detail-rt {
  background-color: pink;
  color: purple;
}

.detail-rt h2 {
  color: purple;
}

</style>

<template>
  <div class="daftar-rt">
    <h1>Daftar RT (Rukun Tetangga)</h1>
    <child-component @pejabat-selected="handlePejabatSelected">
      <template #defaultSlot>
        <p>Ini adalah informasi tambahan yang diteruskan ke ChildComponent melalui slot</p>
      </template>
    </child-component>
    <p>RT Terpilih: {{ selectedPejabat }}</p>
  </div>
</template>

<script>
import ChildComponent from './ChildComponent.vue';

export default {
  components: {
    ChildComponent
  },
  data() {
    return {
      selectedPejabat: ''
    };
  },
  methods: {
    handlePejabatSelected(data) {
      this.selectedPejabat = data;
    }
  }
};
</script>

<style scoped>
.daftar-rt {
  background-color: pink;
  color: purple;
}

.daftar-rt h1 {
  color: purple;
}

.daftar-rt p {
  color: purple;
}

</style>

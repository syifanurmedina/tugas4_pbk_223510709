<template>
  <div class="informasi-rinci-rt">
    <h3>Informasi Rinci RT</h3>
    <button @click="sendPejabatData('Pak Budi')">Pilih RT 1</button>
    <button @click="sendPejabatData('Pak Ratno')">Pilih RT 2</button>
    <button @click="sendPejabatData('Pak Jamal')">Pilih RT 3</button>
  </div>
</template>

<script>
export default {
  methods: {
    sendPejabatData(name) {
      this.$emit('pejabat-selected', name);
    }
  }
};
</script>

<style scoped>
.informasi-rinci-rt {
  background-color: pink;
  color: purple;
  padding: 20px;
  border-radius: 8px;
}

.informasi-rinci-rt h3 {
  color: purple;
}

.informasi-rinci-rt button {
  background-color: rgb(224, 46, 70);
  color: white;
  border: none;
  padding: 10px 20px;
  margin: 5px;
  border-radius: 4px;
  cursor: pointer;
}

.informasi-rinci-rt button:hover {
  background-color: darkmagenta;
}
</style>

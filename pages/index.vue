<template>
  <v-row>
    <v-col cols="8" class="frame-content px-6">
      <Products></Products>
    </v-col>
    <v-col cols="4">ORDERS</v-col>
  </v-row>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>

<style scoped>
html,
body {
  padding: 0;
  overflow: hidden;
}
.frame-content {
  height: 95vh;
  overflow-y: auto;
  background-color: #a0c3d2;
}
.frame-content::-webkit-scrollbar-track {
  background-color: cadetblue !important;
  border-radius: 100px;
}
.frame-content::-webkit-scrollbar-thumb {
  background-color: cadetblue;
  border-radius: 100px;
}
</style>

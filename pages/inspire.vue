<template>
  <v-carousel>
    <v-carousel-item
      v-for="(item, i) in items"
      :key="i"
      :src="item.src"
      reverse-transition="fade-transition"
      transition="fade-transition"
    ></v-carousel-item>
  </v-carousel>
</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          src: 'https://imgur.com/EilRjIA.jpg',
        },
        {
          src: 'https://imgur.com/JiOPgZk.jpg',
        },
        {
          src: 'https://imgur.com/QDNR97W.jpg',
        },
        {
          src: 'https://imgur.com/FMEbo2V.jpg',
        },
      ],
    }
  },
}
</script>
<style></style>

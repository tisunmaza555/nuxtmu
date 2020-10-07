<template>
  <div>
    <v-row>
      <v-col md="4" />
      <v-col md="4" align="center" justify="center">
        <h1>{{ this.$route.params.id.trackName }}</h1>
        <br />
        <v-img
          :src="this.$route.params.id.artworkUrl100"
          max-height="300"
          max-width="300"
        />
      </v-col>
      <v-col md="4" />
    </v-row>
    <v-col align="center" justify="center">
      <h3>{{ this.$route.params.id.artistName }}</h3>
      <h3>CollectionName : {{ this.$route.params.id.collectionName }}</h3>
      <br />
      <audio controls>
        <source :src="this.$route.params.id.previewUrl" type="audio/mpeg" />
      </audio>
      <a
        style="text-decoration: none"
        target="_blank"
        :href="this.$route.params.id.trackViewUrl"
      >
        <h3>Ref : {{ this.$route.params.id.trackViewUrl }}</h3>
      </a>
    </v-col>
  </div>
</template>
<script>
export default {
  data() {
    return {
      id: this.$route.params.id,
    }
  },
}
</script>

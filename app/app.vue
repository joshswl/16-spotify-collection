<template lang="html">
  <div class="app">
    <div class="page">
      <div class="panel">
        <div class="results">
          <song-item v-for="current in tracks2" v-bind:tracks3="current"></song-item>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SongItem from './song-item.vue';
export default {
  components: {
    SongItem,
  },
  created() {
    fetch('https://api.spotify.com/v1/search?query=katy&type=track&offset=0&limit=20')
      .then(response => response.json())
      .then((trax) => {
        this.tracks2 = trax.tracks.items;
      });
  },
  data() {
    return {
      tracks: [],
    };
  },

  data() {
    return {
    };
  },

  methods: {

  },
};
</script>

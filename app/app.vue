<template lang="html">
  <div class="app">
    <div class="section page">
      <div class="results">
        <div class="panel">
          <song-item v-for="current in tracks" v-bind:songs="current"></song-item>
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
        this.tracks = trax.tracks.items;
      });
  },
  data() {
    return {
      tracks: [
        {
          artists: [
            {
              name: 'Bon Iver',
            }
          ],
          name: 'Holocene',
        }
      ],
    };
  },

  methods: {

  },
};
</script>

<template lang="html">
  <div class="results">
    <div class="track">
      <div class="track__media">{{track.media}}</div>
      <div class="track__frame">{{track.frame}}</div>
      <div class="track__artist">{{track.artist}}</div>
      <div class="track__name">{{track.name}}</div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['track'],
  created() {
    fetch('https://api.spotify.com/v1/search?query=katy&type=track&offset=0&limit=20')
      .then(response => response.json())
      .then((tracks) => {
        this.tracks = tracks;
      });
  },
  data() {
    return {
      tracks: {},

    };
  },

  methods: {

  },
};
</script>

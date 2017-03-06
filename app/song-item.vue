<template lang="html">
  <div class="song-item">
    <div class="track">
      <div class="panel-block media">
        <div class="media-left">
          <img v-bind:src="songs.album.images[0].url" alt="" class="track__media track__frame">
        </div>
        <div class="media-content">
          <div class="track__artist">{{songs.artists[0].name}}</div>
          <div class="track__name">{{songs.name}}</div>
        </div>
        <div class="media-right">
          <a v-bind:href="songs.external_urls.spotify" class="fa fa-spotify track__frame"></a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['songs'],

  data() {
    return {
    };
  },

  methods: {

  },
};
</script>

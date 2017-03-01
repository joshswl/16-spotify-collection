<template lang="html">
  <div class="song-item">
    <div class="track">
      <div class="panel-block media">
        <div class="media-left">
          <img src="http://placecage.com/400/400" alt="" class="track__media track__frame">
        </div>
        <div class="media-content">
          <div class="track__artist">asdf artist</div>
          <div class="track__name">track name name name</div>
        </div>
        <div class="media-right">
          <span class="fa fa-spotify spotify-icon"></span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['track'],

  methods: {

  },
};
</script>

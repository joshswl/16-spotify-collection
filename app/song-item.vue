<template lang="html">

</template>

<script>
export default {
  props: ['track'],
  created() {
    fetch('https://api.spotify.com/v1/search?query=katy&type=track&offset=0&limit=20')
      .then(response => response.json())
      .then((tracks) => {
        this.data = tracks;
      });
  },
  data() {
    return {
      tracks: [
        {}
      ],
    };
  },

  methods: {

  },
};
</script>

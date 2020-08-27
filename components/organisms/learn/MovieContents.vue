<template>
    <div class="movie-contents">
      <div class="movie">
          <video src="assets/img/learn/movie.mp4" controls></video>
      </div>
      <MovieNavigation class="none--sp" />
    </div>
</template>

<script>
    import MovieNavigation from '~/components/organisms/learn/MovieNavigation.vue'

    export default {
        components: {
            MovieNavigation
        }
    }

</script>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";

    .movie-contents{
        display: flex;
        justify-content: center;
    }
    .movie{
        width: 100%;
        max-width: vw-pc(1000);
    }
    .movie video{
        width: 100%;
    }
    @media screen and (max-width: $breakpoint1-max) {
        .movie{
            max-width: 100%;
        }
    }
    @media screen and (min-width: $breakpoint2) {
        .movie-contents{
            width: 1400px;
            margin: 0 auto;
        }
    }
</style>
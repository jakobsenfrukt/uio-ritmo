<template>
  <div class="gallery-fixed">
    <div v-for="(media, index) in media" :key="`media-${index}`" class="wrapper item">
      <div class="media">
        <img v-if="media.image" :src="media.image" />
        <Video v-else-if="media.video" :video="media.video" size="full" />
        <Youtube v-else :video="media.youtube" size="full" />
      </div>
      <div v-if="media.caption" class="caption-wrapper">
        <div class="caption">
          <h3 v-if="media.heading">{{ media.heading }}</h3>
          <p>
            {{ media.caption }}<br />
            <a v-if="media.link" :href="media.link.url">{{ media.link.text }}</a>
          </p>
          <span v-if="media.credit" class="credit">{{ media.credit }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Video from '@/components/Video.vue'
import Youtube from '@/components/Youtube.vue'

export default {
  name: 'FixedGallery',
  props: {
    media: Array
  },
  components: {
    Video,
    Youtube
  }
}
</script>

<style scoped lang="scss">
@import '@/css/variables.scss';

.gallery-fixed {
  width: $width-xl;
  margin: 0 auto 4rem;
  max-width: 100%;
  position: relative;

  .wrapper {
    width: 100%;
    padding: 1rem;
  }

  .media {
    position: sticky;
    top: 0;
    height: 100vh;
    width: 50%;
    margin: 0 auto 0 0;
    display: flex;
    padding-right: 1rem;

    img, .video {
      width: 100%;
      display: block;
      align-self: center;
    }
  }

  .caption-wrapper {
    height: 100vh;
    width: 50%;
    margin: 0 0 0 auto;
    padding: 0 1rem;
  }

  .credit {
    font-size: $font-s;
    display: block;
    font-style: italic;
    text-align: right;
    font-family: $sans-serif;
  }
}
</style>

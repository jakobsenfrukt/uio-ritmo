<template>
  <div class="gallery-fixed">
    <div v-for="(media, index) in media" :key="`media-${index}`" class="wrapper item">
      <div class="media">
        <img v-if="media.image" :src="media.image" />
        <Video v-else-if="media.video" :video="media.video" size="full" />
        <Youtube v-else :video="media.youtube" size="full" />
      </div>
      <div class="text-wrapper">
        <div class="text">
          <h3 v-if="media.heading">{{ media.heading }}</h3>
          <span v-if="media.caption">{{ media.caption }}</span>
          <template v-if="media.text">
            <p v-for="(text, index) in media.text" :key="`${index}`">
              {{ text }}
            </p>
          </template>
          <blockquote v-if="media.quote">
            {{ media.quote }}
          </blockquote>
          <a v-if="media.link" :href="media.link.url">{{ media.link.text }}</a>
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
  width: 100%;
  padding: 1rem;
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

  .text-wrapper {
    height: 100vh;
    width: 50%;
    margin: 0 0 0 auto;
    padding: 0 1rem;
    font-family: $serif;

    span {
      display: block;
    }

    blockquote {
      font-size: 1.2rem;
      font-style: italic;
      position: relative;
      &:before {
        content: "“";
        display: block;
        font-size: 6rem;
        color: $color-turquoise;
        position: absolute;
        left: -3rem;
        top: 0;
        line-height: 0.9;
      }
    }
  }

  .credit {
    display: block;
    font-style: italic;
    text-align: right;
    font-family: $sans-serif;
  }
}
</style>

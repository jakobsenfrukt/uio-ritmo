<template>
  <div class="hero">
    <img v-if="image" :src="image" />
    <video v-if="video" muted autoplay>
      <source :src="video" type="video/mp4">
    </video>
    <div class="overlay">
      <transition name="fadeup" appear>
      <div class="text">
        <h1>{{ heading }}</h1>
        <span class="subhead">{{ subhead }}</span>
      </div>
      </transition>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Hero',
  props: {
    image: String,
    video: String,
    heading: String,
    subhead: String
  }
}
</script>

<style scoped lang="scss">
@import '@/css/variables.scss';

.hero {
  margin: 2rem auto 2rem;
  position: relative;
  min-height: 60vh;
  max-height: 100vh;

  img, video {
    width: 100%;
    max-width: $width-xl;
    margin: 0 auto;
    display: block;
    padding-bottom: 6rem;
  }
  img {
    display: none;
  }

  .overlay {
    position: absolute;
    top: 0; right: 0; bottom: 0; left: 0;

    display: flex;
    align-items: flex-end;
  }
  .text {
    width: $width-m;
    max-width: 100%;
    margin: 0 auto;
  }
  h1 {
    font-size: 5rem;
    margin-bottom: 1rem;
    line-height: 1;
  }
  .subhead {
    font-size: 1.6rem;
    line-height: 1.2;
    display: block;
    margin: 0.5rem 0 1.6rem;
    color: $color-blue;
  }

  @media (max-width: $media-s) {
    padding-top: 4rem;
    min-height: 60vh;
    margin-bottom: 0;
    .overlay {
      position: relative;
    }
    img, video {
      padding-bottom: 1rem;
    }
    video {
      display: none;
    }
    img {
      display: block;
    }
    .text {
      padding: 0 1rem;
    }
    h1 {
      font-size: 2.8rem;
    }
    .subhead {
      font-size: 1.2rem;
    }
  }
}
</style>

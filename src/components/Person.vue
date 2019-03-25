<template>
  <div class="person">
    <img :src="image" />
    <h3 class="name">
      <a v-if="link" :href="link">{{ name }}</a>
      <template v-else>{{ name }}</template>
    </h3>
    <p class="bio">{{ bio }}</p>
  </div>
</template>

<script>
export default {
  name: 'Person',
  props: {
    image: String,
    name: String,
    bio: String,
    link: String
  }
}
</script>

<style scoped lang="scss">
@import '@/css/variables.scss';

.person {
  width: 20%;
  padding-right: 2rem;
  img {
    width: 6rem;
    height: 6rem;
    object-fit: cover;
    object-position: 50% 0;
    border-radius: 50%;
    margin-bottom: 1rem;
    border: 0.1rem solid $color-blue;
  }

  .name {
    font-size: 1rem;
    margin: 0 0 0.6rem;

    a {
      color: inherit;
      text-decoration: none;
    }
  }

  .bio {
    font-size: $font-xs;
  }

  @media (max-width: $media-s) {
    width: 100%;
    padding-right: 0;
    margin: 0.6rem auto;
    .name {
      margin: 0.5rem auto 0.3rem;
    }
    img {
      margin-right: 1rem;
      float: left;
    }
    .bio {
      font-size: $font-s;
    }
  }
}
</style>

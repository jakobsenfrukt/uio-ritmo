<template>
  <div class="person">
    <img :src="image" />
    <h3 class="name">
      <a v-if="url" :href="url">{{ name }}</a>
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
    bio: String
  }
}
</script>

<style scoped lang="scss">
@import '@/css/variables.scss';

.person {
  width: 28%;
  img {
    width: 80%;
    border-radius: 50%;
    margin-bottom: 1rem;
  }

  .name {
    font-size: 1.2rem;
    margin: 0 0 0.6rem;

    a {
      color: inherit;
      text-decoration: none;
    }
  }

  .bio {
    font-size: 0.8rem;
  }

  @media (max-width: $media-s) {
    width: 100%;
    img {
      width: 30%;
      margin-right: 1rem;
      float: left;
    }
  }
}
</style>

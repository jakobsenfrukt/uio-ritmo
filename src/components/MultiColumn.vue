<template>
  <section class="multi-column">
    <div v-for="(block, index) in blocks" :key="`block-${index}`" class="multi-column-block">
      <div class="image">
        <Figure
          :image="block.image"
          alt="Bildet viser no greier"
          size="full"
        />
      </div>
      <div class="text">
        <h3>
          <a v-if="block.link" :href="block.link">{{ block.heading }}</a>
          <template v-else>{{ block.heading }}</template>
        </h3>
        <p>{{ block.text }}</p>
      </div>
    </div>
  </section>
</template>

<script>
import Figure from '@/components/Figure.vue'

export default {
  name: 'MultiColumn',
  components: {
    Figure
  },
  props: {
    blocks: Array
  }
}
</script>

<style scoped lang="scss">
@import '@/css/variables.scss';

.multi-column {
  width: $width-xl;
  max-width: 100%;
  margin: 0 auto;
  display: flex;
  align-items: center;
  flex-wrap: wrap;

  &-block {
    max-width: 25%;
    display: block;
    align-self: center;
    padding-right: 2rem;
  }

  h3 {
    font-size: 1.6rem;
    margin: 0.5rem auto;
  }

  p {
    font-size: $font-s;
  }

  img {
    max-width: 100%;
  }

  .figure {
    margin: 0;
  }

  @media (max-width: $media-s) {
    margin: 1rem auto 2rem;
    padding: 0 1rem;
    &-block {
      max-width: 50%;
      display: block;
      align-self: center;
      padding-right: 2rem;
    }
  }
}

</style>

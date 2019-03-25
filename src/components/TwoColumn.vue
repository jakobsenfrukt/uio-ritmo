<template>
  <section class="two-column">
    <div class="image">
      <Figure
        image="/images/infographics/RITMO-Matrise-2.svg"
        alt="Bildet viser no greier"
        size="column"
        caption="Research priorities (hori­zontal) and empirical fields (vertical) that are investigated in RITMO."
      />
    </div>
    <div class="text">
      <p><strong>Structure</strong> concerns our ability to structure the past and predict future events, and to discern variation with regard to an underlying pattern.</p>
      <p>This, in turn, facilitates <strong>interaction</strong> with both other human beings and external events, which is crucial for example in synchronisation, conversation and bodily coordination.</p>
      <p>The research priority <strong>pleasure</strong> focuses on rhythm as a phenomenon related to social functions and well-being. Why do certain rhythms invite participation, such as dancing, while others do not.</p>
      <p>Underlying all of the other themes, is the topic of <strong>time</strong>, which addresses that rhythm also impacts the ordering of temporal events far beyond the ‘now’ of its perceptual and cognitive unfolding. Here the focus is rhythm’s role in ‘remembering’ large-scale formations of time.</p>
      <p>RITMO will pursue these four overarching research priorities in three empirical fields&mdash;<em>music</em>, <em>motion</em>, and <em>audiovisual media</em>&mdash;which represent different but related modalities of rhythm.</p>
    </div>
  </section>
</template>

<script>
import Figure from '@/components/Figure.vue'

export default {
  name: 'TwoColumn',
  components: {
    Figure
  }
}
</script>

<style scoped lang="scss">
@import '@/css/variables.scss';

.two-column {
  width: $width-xl;
  max-width: 100%;
  margin: 3rem auto 0;
  display: flex;
  align-items: center;

  .image {
    width: 50%;
    display: block;
    align-self: center;
    padding: 0 4rem 0 2rem;
  }
  .text {
    width: 50%;
    padding-left: 2rem;
  }

  &.reverse {
    text-align: right;
  }

  @media (max-width: $media-s) {
    display: block;
    margin: 1rem auto 2rem;
    padding: 0 1rem;
    .image, .text {
      width: 100%;
      padding: 0;
    }
  }
}

</style>

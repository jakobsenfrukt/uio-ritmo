<template>
  <section class="text item logos">
    <h3 v-if="heading">{{ heading }}</h3>
    <div class="logo-list">
      <img src="https://www.hf.uio.no/ritmo/bilder/hf_imv_seal_a_eng.png" />
      <img src="https://www.hf.uio.no/ritmo/bilder/mn_ifi_seal_a_eng.png" />
      <img src="https://www.hf.uio.no/ritmo/bilder/sv_psyk_seal_a_eng.png" />
    </div>
  </section>
</template>

<script>
export default {
  name: 'LogoList',
  props: {
    heading: String
  }
}
</script>

<style scoped lang="scss">
@import '@/css/variables.scss';

.logos {
  margin: 0 auto 4rem;
  h3 {
    width: $width-l;
    max-width: 100%;
  }
  .logo-list {
    width: $width-l;
    margin: 0 auto;
    max-width: 100%;
  }
  img {
    width: $width-xxs;
    display: block;
    margin-bottom: 1rem;
  }
}
</style>

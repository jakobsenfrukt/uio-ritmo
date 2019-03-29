<template>
  <section class="text item logos">
    <div>
      <h3>A Centre of Excellence in Norway</h3>
      <img src="/images/sff-logo.svg" />
    </div>
    <div>
      <h3>RITMO is a collaboration between</h3>
      <div class="logo-list">
        <img src="https://www.hf.uio.no/ritmo/bilder/hf_imv_seal_a_eng.png" />
        <img src="https://www.hf.uio.no/ritmo/bilder/mn_ifi_seal_a_eng.png" />
        <img src="https://www.hf.uio.no/ritmo/bilder/sv_psyk_seal_a_eng.png" />
      </div>
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
  width: $width-l;
  max-width: 100%;
  display: flex;
  justify-content: space-between;
  > div {
    width: 40%;
  }
  h3 {
    max-width: 100%;
    font-size: 1.4rem;
  }
  .logo-list {
    margin: 0 auto;
    width: 100%;
  }
  img {
    max-width: $width-xxs;
    max-height: 8rem;
    display: block;
    margin: 0 0 1rem;
  }

  @media (max-width: $media-m) {
    display: block;
    > div {
      width: 100%;
      margin-bottom: 4rem;
    }
  }
}
</style>

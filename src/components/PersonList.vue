<template>
  <section class="text item background people">
    <h3>Ansatte</h3>
    <div class="person-list">
      <Person
        image="https://pbs.twimg.com/profile_images/941101314938949638/wc2T0MFY_400x400.jpg"
        name="Svein Stølen"
        bio="Dette er bioen!"
      />
    </div>
  </section>
</template>

<script>
import Person from '@/components/Person.vue'
export default {
  name: 'PersonList',
  components: {
    Person
  }
}
</script>

<style scoped lang="scss">
@import '@/css/variables.scss';

.people {
  h3 {
    width: $width-l;
    max-width: 100%;
  }
  .person-list {
    margin: 0 auto;
    padding: 0;
    list-style: none;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    width: $width-l;
    max-width: 100%;
  }
}
</style>

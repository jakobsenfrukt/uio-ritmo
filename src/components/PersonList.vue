<template>
  <section class="text item people">
    <h3 v-if="heading">{{ heading }}</h3>
    <div class="person-list">
      <Person
        v-for="(person, index) in people" :key="`person-${index}`"
        :image="person.image"
        :name="person.name"
        :link="person.link"
        :bio="person.bio"
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
  },
  props: {
    heading: String,
    people: Array
  }
}
</script>

<style scoped lang="scss">
@import '@/css/variables.scss';

.people {
  margin-bottom: 2rem;
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
    justify-content: left;
    width: $width-l;
    max-width: 100%;
  }
}
</style>

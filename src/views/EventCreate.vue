<template>
  <div>
    <h1>Create an Event, {{ user.name }}</h1>
    <p>Created by {{ user.id }}</p>
    <p>{{ getEventById(2) }}</p>

    <p>There are {{ catLength }} categories</p>
    <ul>
      <li v-for="cat in categories" :key="cat">{{ cat }}</li>
    </ul>
  </div>
</template>

<script>
import { mapState, mapGetters } from 'vuex'

export default {
  computed: {
    ...mapGetters(['catLength', 'getEventById']),
    ...mapState(['user', 'categories'])
  }
}
</script>

<style lang="scss" scoped></style>

<template>
  <div class="home">
    <same-header></same-header>
    <search></search>
  </div>
</template>

<script>
import SameHeader from '../components/SameHeader.vue'
import Search from '../components/Search.vue'

export default {
  components: {
    SameHeader,
    Search
  }
}
</script>

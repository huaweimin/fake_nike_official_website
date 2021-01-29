<template>
  <div class="home">
    <same-header></same-header>
    <search></search>
    <adver></adver>
  </div>
</template>

<script>
import SameHeader from '../components/SameHeader.vue'
import Search from '../components/Search.vue'
import Adver from '../components/Advertise.vue'

export default {
  components: {
    SameHeader,
    Search,
    Adver
  }
}
</script>

<template>
  <div class="">
   <museum />
   <meet />
   <news />
  </div>
</template>

<script>
import Museum from '../components/Museum.vue'
import Meet from '../components/Meet.vue'
import News from '../components/News.vue'
export default {
  components: {
    Museum,
    Meet,
    News
  }
}
</script>

<style>
</style>
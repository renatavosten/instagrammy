<template>
  <div class="row">
    <div class="col-1"></div>
    <div class="col-7">
      <div class="home">
        <InstagramCard/>
        <InstagramCard/>
      </div>
    </div>
    <div class="col-4">
      <InstagramStory/>
      <InstagramSugg/>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import InstagramCard from '@/components/InstagramCard.vue'
import InstagramStory from '@/components/InstagramStory.vue'
import InstagramSugg from '@/components/InstagramSugg.vue'

export default {
  name: 'home',
  components: {
    InstagramCard,
    InstagramStory,
    InstagramSugg
  }
}
</script>

<style lang="scss">
  .card{
    margin-bottom: 20px;
    
  }
</style>





<template>
  <div class="row">
    <div class="col-8">
      <InstagramCard :key="card.id" :info="card" v-for="card in filteredCards" /> 
    </div>
    <div class="col-4">
      <InstagramStory/>
      <InstagramSugg/>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import InstagramCard from '@/components/InstagramCard.vue';
import InstagramStory from '@/components/InstagramStory.vue';
import InstagramSugg from '@/components/InstagramSugg.vue';
import store from "@/store.js";

export default {
  data () {
    return store;  
  },
  computed: {
    filteredCards() {
      let filtered = [];
      for (let card of this.cards) {
        if (card.title.includes(this.searchTerm)) {
          filtered.push(card);
        }
      }
      return filtered;
      //return this.cards.filter(card => card.title.includes(this.searchTerm)); malo drukčija sintaksa
    }
  },
  name: 'home',
  components: {
    InstagramCard,
    InstagramStory,
    InstagramSugg
  }
};
</script>

<style lang="scss">
  .card{
    margin-bottom: 20px;
    
  }
</style>





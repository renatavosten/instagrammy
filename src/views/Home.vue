<template>
  <div class="row">
    <div class="col-8">
      <div v-if="authenticated">
        <form @submit.prevent="postImage">
        <div class="form-group">
          <label for="imageUrl">Image URL</label>
          <input v-model="postImageUrl" type="text" class="form-control" id="imageUrl" placeholder="Paste the image URL">
        </div>
        <button type="submit" class="btn btn-primary mb-3">Post</button>
        </form>

        <InstagramCard :key="card.id" :info="card" v-for="card in filteredCards" /> 
      </div>
    </div>
    <div class="col-4">
      <div v-if="authenticated">
        <InstagramStory/>
        <InstagramSugg/>
      </div>
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
        if (card.postedBy.includes(this.searchTerm)) {
          filtered.push(card);
        }
      }
      return filtered;
      //return this.cards.filter(card => card.title.includes(this.searchTerm)); malo drukčija sintaksa
    }
  },

  methods: {
    postImage() {                     //dodaje novi post u Firebase kolekciju
      db.collection("posts-real").add({
        id: this.cards.length + 1,
        postedBy: this.userEmail, 
        time: Date.now(), 
        url: this.postImageUrl
      })
      .then(function(docRef) {
          console.log("Document written with ID: ", docRef.id);
      })
      .catch(function(error) {
          console.error("Error adding document: ", error);
      });
      this.postImageUrl = ''
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





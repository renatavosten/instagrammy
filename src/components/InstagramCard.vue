<template>
  <div class="card">
        <div class="card-header text-left">
          <img :src=info.avatar class="mr-3" alt ="..." />
          <small>
            <b>{{ info.postedBy }}</b>
          </small>
        </div>
      <div class="card-body p-0">
        <!-- p-0 je padding 0-->
        <img @click="changeImage" class="card-img-top" :src="info.url" alt ="..."/>
      </div>
      <div class="card-footer text-muted text-left">{{ postedFromNow }}</div>
  </div>
</template>

<script>
export default {
  props: ["info"],

  computed: {
    postedFromNow() {
      return moment(this.info.time).fromNow();
    }
  },
  methods: {
    changeImage() {
      this.info.time = 'Fetching...'
      fetch(`https://source.unsplash.com/1600x900/?nature,water`).then(
        response => {
          console.log(response);
          this.info.url = response.url;
          this.info.time = 'Done.'
        }
      );
    }
  }
};
</script>

<style lang="scss" scoped>
  img:hover {
    cursor: pointer;
  }
  .mr-3{
    height: 34px;
    width: 34px;
    border-radius: 50%;
  }
</style>



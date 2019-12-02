<template>
  <div class="card">
        <div class="card-header text-left">
          {{ info.title }}
        </div>
      <div class="card-body p-0">
        <!-- p-0 je padding 0-->
        <img @click="changeImage" class="card-img-top" :src="info.url" alt ="vrtuljak"/>
      </div>
      <div class="card-footer text-muted text-left">
        {{ info.time }}
      </div>
  </div>

</template>

<script>
export default {
  props: ["info"],
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
</style>



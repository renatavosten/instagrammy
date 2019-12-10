<template>
  <div class="card">
    <div class="card-body">
      <h6 class="card-subtitle mb-2 text-muted">Stories</h6>
      <ul class="list-unstyled">
        <li class="media mt-3">
          <img src="photo-1552168324-d612d77725e3.jpg" class="mr-3" alt="fotograf"/>
          <div class="media-body">
            <h6 class="mt-0 mb-1 text-left">
              fotographymaster
              <br />
              <small class="text-muted"> 12 minutes ago</small>
            </h6>
          </div>
        </li>
        <li class="media my-4">
          <img src="photo-1569077218751-3e3de7800c00.jpg" class="mr-3" alt="hrana"/>
          <div class="media-body">
            <h6 class="mt-0 mb-1 text-left">
              foodblogger
              <br />
              <small class="text-muted">1 minute ago</small>
            </h6>
          </div>
        </li>
        <li class="media">
          <img src="photo-1574327694472-d172fb4d5865.jpg" class="mr-3" alt="model"/>
          <div class="media-body">
            <h6 class="mt-0 mb-1 text-left">
              fashionmodels
              <br />
              <small class="text-muted">2 hours ago</small>
            </h6>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name:"InstagramStory",
  props: {
    msg: String
  }
};
</script>

<style scoped lang="scss">
  .mr-3{
    height: 34px;
    width: 34px;
    border-radius: 50%;
    border: 2px solid #FF4500;
  }
  .card{
    max-width: 348px;
    max-height: 271.200px;
    overflow: auto;
  }

</style>




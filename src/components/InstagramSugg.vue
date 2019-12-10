<template>
  <div class="card">
    <div class="card-body">
      <h6 class="card-subtitle mb-2 text-muted">Suggestions</h6>
      <ul class="list-unstyled">
        <li class="media mt-3">
          <img src="photo-1483086431886-3590a88317fe.jpg" class="mr-3" alt="polarna svjetlost"/>
          <div class="media body">
            <div class="row">
              <div class="col-6">
                <h6 class="mt-0 mb-1 text-left">
                  polarlightlover
                  <br />
                  <small class="text-muted">Followed by timmothy + 5 more</small>
                </h6>
              </div>
              <div class="col-6 text-right">
                <button type="button" class="btn btn-primary btn-sm">Follow</button>
              </div>
            </div>
          </div>
        </li>
        <li class="media my-4">
          <img src="photo-1538805060514-97d9cc17730c.jpg" class="mr-3" alt="fitness"/>
          <div class="media-body">
            <div class="row">
              <div class="col-6">
                <h6 class="mt-0 mb-1 text-left">
                  fitnesslife
                  <br />
                  <small class="text-muted">Followed by peter + 10 more</small>
                </h6>
              </div>
              <div class="col-6 text-right">
                <button type="button" class="btn btn-primary btn-sm">Follow</button>
              </div>
            </div>
          </div>
        </li>
        <li class="media">
          <img src="photo-1573905891290-b8e0b2d56224.jpg" class="mr-3" alt="arhitektura"/>
          <div class="media-body">
            <div class="row">
              <div class="col-6">
                <h6 class="mt-0 mb-1 text-left">
                  arhitecturedose
                  <br />
                  <small class="text-muted">Followed by Cameron</small>
                </h6>
              </div>
              <div class="col-6 text-right">
                <button type="button" class="btn btn-primary btn-sm">Follow</button>
              </div>
            </div>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  props: ["info"]
};
</script>

<style scoped lang="scss">
  .mr-3{
    height: 34px;
    width: 34px;
    border-radius: 50%;
  }

</style>
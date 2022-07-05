<template>
  <div class="our-assets">
    <h2>Наши активы</h2>
    <div class="assets">
      <div class="asset" v-for="ourAsset in ourAssets">
        <div class="backgroundField"><img class="img12" :src="require(`../img/${ourAsset.name}`)"></div>
        <div class="asset-text">Enter</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "OurAssets",
  props: {
    ourAssets: {
      type: Array,
      required: true,
    }
  },
}
</script>

<style scoped>
.our-assets {
  max-width: 100vw;
  background: #001CAD;
  color: #ffffff;
  padding: 50px 0 150px 8px;
  z-index: 10;
  position: relative;

}

.assets{
  display: grid;
  margin-top: 50px;
  grid-template-columns: repeat(8, 240px);
  column-gap: 30px;
  overflow-x: auto;
}

.asset{
position: relative;
}

h2{
  margin-left: 50px;
}

.backgroundField{
  height: 480px;
  background-color: rgba(0.0.0.0);
}

.img12{
  object-fit: cover;
  opacity: 0.3;
  width: 100%;
  height: 100%;
}

.asset-text{
  position: absolute;
  top: 50%;
  left: 40%;
}

@media (max-width: 768px) {

  h2{
    margin-left: 0;
  }

  .our-assets {
    max-width: 100vw;
    background: #001CAD;
    color: #ffffff;
    padding: 40px 0 40px 8px;
    z-index: 10;
    position: relative;
    overflow-x: auto;
  }

  .assets{
    grid-template-columns: repeat(8, 165px);
    column-gap: 15px;
    margin-top: 30px;
  }

  .backgroundField{
    height: 300px;
    background-color: rgba(0.0.0.0);
  }

}

</style>
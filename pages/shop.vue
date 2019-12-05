<template>
  <div class="shopContainer">
    <div class="shop">
      <Goods />
    </div>
    <Info />
  </div>
</template>
<script>
import Goods from "../components/Goods";
import Info from "../components/Info";

export default {
  name: "shop",
  components: {
    Goods,
    Info
  }
};
</script>

<style lang="scss" scoped>
.shop {
  width: 100vw;
  min-height: 43vh;
  margin-top: 5vh;
  margin-bottom: 5vh;
  display: flex;
  justify-content: center;
}
</style>

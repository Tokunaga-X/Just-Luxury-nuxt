<template>
  <div class="circle">{{ getCount }}</div>
</template>
<script>
import { mapActions, mapGetters } from "vuex";

export default {
  name: "carInfo",
  computed: {
    ...mapGetters(["getCount"])
  },
  methods: {
    plus() {
      // mutations
      // store.commit("plus");
      // actions
      store.dispatch("plus", 1000);
    }
  }
};
</script>
<style lang="scss" scoped>
.circle {
  position: fixed;
  top: 25%;
  left: 85%;
  width: 2rem;
  height: 2rem;
  display: flex;
  font-size: 1.5rem;
  color: white;
  justify-content: center;
  align-items: center;
  border-radius: 50%;
  background: orange;
  cursor: pointer;
  z-index: 10;
}
</style>

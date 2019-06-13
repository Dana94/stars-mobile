<template>
  <div>
    <div class="string" v-if="active"></div>
    <img src="../assets/moon.svg" class="moon">
  </div>
</template>

<script>
export default {
  data() {
    return {
      active: true
    };
  },
  methods: {
    mouseOver() {
      console.log("over");
    },
    mouseEnter() {
      console.log("enter");
    }
  }
};
</script>

<style lang="scss" scoped>
.string {
  height: 220px;
  width: 10px;
  background-color: #563c28;
  margin: 0 auto;
}

.moon {
  height: 300px;
  margin-top: -4rem;
}

.moon:hover {
  // animation: move-image 0.6s;
  animation: 3s move-image;
}
@keyframes move-image {
  from {
    transform: rotate(45deg);
  }
}
@keyframes slidein {
  from { transform: scaleX(0); }
  to   { transform: scaleX(1); }
}
</style>

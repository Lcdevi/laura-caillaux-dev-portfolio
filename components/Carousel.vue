<template>
  <div class="carousel">
    
    <slot></slot>

    <button @click="prev" class="prev">prev</button>
    <button @click="next" class="next">next</button>

  </div>
</template>

<script>
export default {
  data() {
    return {

    }
  },
  methods: {
    next() {
      console.log("next")
      this.$emit('next')
    },
    prev() {
      console.log("prev")
      this.$emit('prev')
    }
  }
}

</script>

<style lang="scss" scoped>
  .carousel {
    border: 1px solid green;
    position: relative;
    display: flex;
    // width: 610px;
    // height: 350px;
    // overflow: hidden;
    // & button {
    //   border: 1px solid $brown;
    //   background-color: inherit;
    //   cursor: pointer;
    //   font-family: inherit;
    //   padding: 8px 8px;
    //   border-radius: 6px;
    //   position: absolute;
    // }
    // & .prev {
    //   top: calc(50% - 20px);
    //   left: -100px;
    // }
    // & .next {
    //   top: calc(50% - 20px);
    //   right: -100px;
    // }
  }
</style>

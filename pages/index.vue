<template>
  <div class="container">
    <div>
      <Navbar />
      <div id="presentation">
        <p><span>HI !</span> Welcome to my website, I’m <span>Laura</span>, a french
web designer & front-end developer, passionate about clean code, responsive design and accessibility</p>
      </div>
      <Footer />
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang='scss' scoped>
  .container {
    font-family: $ff-sans;
    position: relative;
    height: 100vh;
    & #presentation {
      border: 1px solid green;
      display: flex;
      justify-content: center;
      & p {
        font-size: $font-size-pres;
        line-height: $line-height-pres;
        width: 847px;
        text-align: center;
        & span {
          font-family: $ff-serif;
          font-size: 42px;
        }
      }
    }
  }
</style>

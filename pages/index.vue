<template>
  <div class="container">
    <div id="presentation">
      <p class="hero">
        <span>HI !</span> Welcome to my website, I’m <span>Laura</span>, a french <br>
        web designer & front-end developer, passionate about clean code, responsive design and accessibility
      </p>
      <p>
        I used to develop with these technologies but I’m open to work with other frameworks or languages
      </p>
      <div class="tools">
        <div class="circle"></div>
        <div class="circle"></div>
        <div class="circle"></div>
        <div class="circle"></div>
      </div>
    </div>
    <div class="link">
      <NuxtLink to="/work">take a look to my work -></NuxtLink>
    </div>
  </div>
</template>

<style lang='scss' scoped>
.big {color: red;}
  .container {
    // border: 1px solid pink;
    font-family: $ff-sans;
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 34px 0;

    & #presentation {
      // border: 1px solid green;
      display: flex;
      flex-direction: column;
    
      & p {
        font-size: $font-size-pres;
        line-height: $line-height-pres;
        width: 847px;
        text-align: center;
        margin: 18px 0;
      
        & span {
          font-family: $ff-serif;
          font-size: 42px;
        }
      }

      & .tools {
        // border: 1px solid red;
        display: flex;
        justify-content: center;
        margin: 18px 0;

        & .circle {
          background-color: rgb(191, 191, 191);
          width: 80px;
          height: 80px;
          border-radius: 50%;
          margin: 0 20px;
        }
      }

    }

    & .link {
      // border: 1px solid red;
      width: 847px;
      display: flex;
      justify-content: flex-end;
      margin: 18px 0;
    }
  }
</style>

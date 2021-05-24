<template>
  <div class="index-container">
    <div id="presentation">
      <p class="hero">
        <span class="serif">HI !</span> Welcome to my website, I’m <span class="serif">Laura</span>, a french <br>
        <span class="underline">web designer</span> & <span class="underline">front-end developer</span>, passionate about clean code, responsive design and accessibility
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
  .index-container {
    // border: 1px solid pink;
    font-family: $ff-sans;
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 216px 0;

    & #presentation {
      // border: 1px solid green;
      display: flex;
      flex-direction: column;
    
      & p {
        font-size: $font-size-pres;
        line-height: $line-height-pres;
        width: 847px;
        text-align: center;
        margin: 32px 0;
      
        & .serif {
          font-family: $ff-serif;
          font-size: 42px;
        }

        & .underline {
          position: relative; 
        }
        & .underline:after {
          position: absolute;
          content: '';
          height: 1px;
          bottom: 3px; 
		      left: 0;
          right: 0;
		      background: $brown;
        }
      }

      & .tools {
        // border: 1px solid red;
        display: flex;
        justify-content: center;
        margin: 32px 0;

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
      margin: 32px 0;
    }
  }
</style>

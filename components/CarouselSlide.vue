<template>
  <div v-show="visibleSlide === index" class="carousel-slide">
    <img src="~/assets/img/Rectangle-43.jpg" alt="">
		<p class="rank">{{ project.id }} / {{ slidesLen }}</p>
    <div class="title">
      <h2>{{ project.title }}</h2>
      <p class="description">{{ project.description }}</p>
      <br>
    </div>
    <div class="infos">
      <div class="left-part">
        <h3>description</h3>
        <p>{{ project.infos }}</p>
        <br>
      </div>
      <div class="right-part">
        <h3>stack utilisée</h3>
        <p>{{ project.stack }}</p>
        <br>
        <div v-if="project.thirdparties">
          <h3>API tierce</h3>
          <p>{{ project.thirdparties }}</p>
          <br>
        </div>
        <h3>rôle</h3>
        <p>{{ project.role }}</p>
        <br>
        <h3>année</h3>
        <p>{{ project.date }}</p>
      </div>
    </div>
    <div class="link">
      <a :href="project.url" target="_blank" rel="noopener noreferrer">
        voir le site
      </a>
    </div>
  </div>
</template>

<script>
  export default {
    props: ['index', 'visibleSlide', 'project', 'slidesLen'],
  }
</script>

<style lang="scss" scoped>
.carousel-slide {
  // border: 1px solid blue;
  margin: 0 80px;
  position: relative;
  display: flex;
  flex-direction: column;
  width: 700px;
  & .rank {
    font-size: 45px;
    position: absolute;
    top: -25px;
    right: -45px;
  }
  & h2 {
    margin: 40px 0 30px 0;
  }
  & .description {
    font-weight: 700;
    font-size: 18px;
  }
  & p {
    line-height: $line-height-reg;
  }
  & .link {
    // border: 1px solid blue;
    width: 100%;
    display: flex;
    justify-content: flex-end;
    margin-top: 40px;
  }
  & .title {
    text-align: center;
    margin: 0 0 20px 0;
  }
  & .infos {
    // border: 1px solid pink;
    display: flex;
   
    & .left-part {
      // border: 1px solid red;
      width: 50%;
      padding: 0 16px;
    }
    & .right-part {
      // border: 1px solid green;
      padding: 0 16px;
      width: 50%;
    }
  }

}

</style>

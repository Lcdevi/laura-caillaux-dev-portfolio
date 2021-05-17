<template>
  <div id="project">
    <div id="image"></div>
    <div id="infos">
      <h2>{{ project.title }}</h2>
      -
      <p class="inf">{{ project.infos }}</p>
      -
      <p class="inf">{{ project.stack }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ['project'],

  mounted() {
    console.log(this.project)    
  }

}
</script>

<style lang="scss" scoped>
#project {
  margin: 40px 0;
  & #image {
    width: 600px;
    height: 300px;
    background-color: rgb(199, 199, 199);
  }
  & #infos {
    display: flex;
    flex-direction: column;
    align-items: center;
    & p {
      margin: 10px 0;
    }
    & h2 {
      margin: 20px 0 10px 0;
    } 
  }
}
</style>
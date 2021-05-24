<template>
	<div class="work-container">
		<button @click="prev">PREV</button>

			<carousel-slide 
				v-for="(project, index) in projects" 
				:key="project.id" 
				:index="index"
				:visibleSlide="visibleSlide"
				:project="project"
				:slidesLen="slidesLen"
			>
				<!-- <img src="~/assets/img/Rectangle-43.jpg" alt="">
				<p>{{ project.id }} / {{ slidesLen }}</p>
				<h2>TITRE : {{ project.title }}</h2>
				<p>informations: {{ project.infos }}</p>
				<p>stack : {{ project.stack }}</p> -->
			</carousel-slide>

			<button @click="next">NEXT</button>
	</div>
	<!-- <div class="work-container">
		<carousel
			@next="next"
			@prev="prev"
		>
		<button @click="prev">TEST PREV</button>
			<carousel-slide 
				v-for="(project, index) in projects" 
				:key="project.id" 
				:index="index"
				:visibleSlide="visibleSlide"
			>
				<img src="~/assets/img/Rectangle-43.jpg" alt="">
				<p>{{ project.id }} / {{ slidesLen }}</p>
				<h2>TITRE : {{ project.title }}</h2>
				<p>informations: {{ project.infos }}</p>
				<p>stack : {{ project.stack }}</p>
			</carousel-slide>
			<button @click="next">TEST NEXT</button>
		</carousel>
	</div> -->
</template>

<script>
import projectData from "~/data/projects.json";

export default {
	data() {
    return {
      projects: projectData,
			visibleSlide: 0,
    }
  },
	computed: {
		slidesLen() {
			return this.projects.length;
		}
	},
	methods: {
		next() {
			if(this.visibleSlide >= this.slidesLen - 1) {
				this.visibleSlide = 0;
			} else {
				this.visibleSlide++;
			}
		},
		prev() {
			if(this.visibleSlide <= 0) {
				this.visibleSlide = this.slidesLen - 1;
			} else {
				this.visibleSlide--;
			}

		}
	}
}
</script>

<style lang="scss" scoped>

.work-container {
	// border: 1px solid red;
	display: flex;
	flex-direction: row;
	justify-content: center;
	align-items: center;
	margin: 70px 0;
	& button {
		border: 1px solid $brown;
		background-color: inherit;
		font-family: inherit;
		height: 40px;
		width: 80px;
		border-radius: 8px;
	}
}

</style>

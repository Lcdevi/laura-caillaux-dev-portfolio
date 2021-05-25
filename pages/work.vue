<template>
	<div class="work-container">
		<h1>Projets</h1>
		<div class="carousel">
			<button @click="prev">PREV</button>

			<carousel-slide 
				v-for="(project, index) in projects" 
				:key="project.id" 
				:index="index"
				:visibleSlide="visibleSlide"
				:project="project"
				:slidesLen="slidesLen"
			>
			</carousel-slide>

			<button @click="next">NEXT</button>
		</div>
	</div>
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
	flex-direction: column;
	justify-content: center;
	align-items: center;
	margin: 70px 0;
	& .carousel {
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
		margin: 70px 0;
	}
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

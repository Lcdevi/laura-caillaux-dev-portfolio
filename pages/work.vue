<template>
  <div id="work">
		<h1>work</h1>
		<div id="carrousel">
			<div class="item" v-for="project in projects" :key="project.id">
				<Project
					:project="project"
				/>
			</div>
		</div>
	</div>
</template>

<script>
import projectData from "~/data/projects.json";

export default {
	data() {
    return {
      projects: projectData,
    }
  },
}
</script>

<style lang="scss" scoped>

#work {
	display: flex;
	flex-direction: column;
	align-items: center;
	margin: 70px 0;
	& #carrousel {
		display: flex;
		overflow: hidden;
	}
}

</style>

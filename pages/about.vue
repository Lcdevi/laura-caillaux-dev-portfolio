<template>
	<div id="about-container">
		<h1>A propos</h1>
		<div class="content">
			<img src="~/assets/img/Rectangle-7.png" alt="rectange gris">
			<div>
				<p class="p-reg">
					Bonjour, je suis Laura Caillaux,<br>je suis née à Kathmandu il y a 32 ans.<br>Dans une vie précédente, j'enseignais l'art de la reliure dans une école d'art à Strasbourg.<br>Je fais maintenant du développement web et de l'intégration web en freelance à Paris.
				</p>
				<NuxtLink to="/contact">
					<p class="link">Votre projet, on en parle ? -></p>
				</NuxtLink>
			</div>
		</div>
	</div>
</template>

<style lang="scss" scoped>

#about-container {
	// border: 1px solid red;
	display: flex;
	flex-direction: column;
	align-items: center;
	margin: 70px 0;

	& .content {
		// border: 1px solid green;
		display: flex;
		width: 80vw;
		max-width: 860px;
		margin: 70px 0;

		& img {
			max-width: 400px;
		}

		& .p-reg {
			margin-bottom: 60px;
		}

		& p {
			margin-left: -80px;
		}

		& .link {
			font-size: 20px;
		}

		& div {
			// border: 1px solid red;
			display: flex;
			flex-direction: column;
			justify-content: center;
		}
	}
}

</style>

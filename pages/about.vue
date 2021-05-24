<template>
	<div id="about-container">
		<h1>About</h1>
		<div class="content">
			<img src="~/assets/img/Rectangle-7.png" alt="rectange gris">
			<div>
				<p class="p-reg">
					Hello, I’m Laura Caillaux,<br> born in kathmandu 32 years ago.<br>In a previous life I was a teacher in a art school in Strasbourg. I’m now a free-lance web developer based in Paris. According to your project, I can create website from scratch, but I can work also with CMS as wordpress or webflow or woocommerce for your e-shop.
				</p>
				<NuxtLink to="/contact">
					<p class="link">Let's talk about your project -></p>
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

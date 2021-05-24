<template>
	<div id="contact-container">
		<h1>contact</h1>
		<div class="content">
			<div class="text">
				<p class="p-reg">
					Un projet de site web, site vitrine, e-commerce ou landing page ? <br>
					Vous avez aimé mon portfolio ? <br>
					Vous souhaitez un devis personnalisé ? <br>
					Contactez moi par mail.
				</p>
					<div class="mail">caillauxlaura@gmail.com</div>
				<p class="p-reg">
					ou utilisez ce formulaire de contact, <br>
					je vous réponds dans les plus bref délais !
				</p>
			</div>
			<contact-form>
			</contact-form>
		</div>
	</div>
</template>

<style lang="scss" scoped>

#contact-container {
	// border: 1px solid red;
	display: flex;
	flex-direction: column;
	align-items: center;
	margin: 202px 0;
	& .content {
		// border: 1px solid green;
		width: 80vw;
		max-width: 860px;
		margin: 70px 0;
		display: flex;
		flex-direction: column;
		align-items: center;
		& .text {
			text-align: center;
			& .mail {
				font-family: $ff-serif;
				font-size: $font-size-h2;
				margin: 40px 0;
			}
		}
	}
}

</style>

<template>
  <div class="services-container">
    <h1>Mes services</h1>
    <div class="content">
      <div class="service-pres">
        <img src="~/assets/img/Rectangle-47.png" alt="">
        <p class="p-reg">
          Vous êtes un particulier, une association, une petite entreprise, commerce, artisan ou artiste, vous avez besoin d'un site web vitrine pour présenter votre activité ? Vendre vos réalisations ? Vous faire connaître ?
        </p>
      </div>
    </div>
    <div class="services">
			<div class="service">
				<div class="one-service">
					<div class="title">
						<img src="~/assets/img/Rectangle-47.png" alt="">
						<h3>VueJS & Nuxt</h3>
					</div>
					<p class="p-reg">VueJS est un des framework les plus utilisé aujourd'hui, il permet de développer des sites complexes avec une grande maintenabilité. Nuxt est sa version statique, et permet un référencement optimal.</p>
				</div>
				<div class="one-service">
					<div class="title">
						<img src="~/assets/img/Rectangle-47.png" alt="">
						<h3>Wordpress & Webflow</h3>
					</div>
					<p class="p-reg">Wordpress est l'un des CMS les plus utilisé à travers le monde ! Webflow quant à lui permet une plus grande liberté dans le design. Avec ces solutions, la gestion de contenu est facilité.</p>
				</div>
				<div class="one-service">
					<div class="title">
						<img src="~/assets/img/Rectangle-47.png" alt="">
						<h3>E-commerce</h3>
					</div>
					<p class="p-reg">Vous souhaitez une boutique en ligne facilement maintenanble ? Avec WooCommerce ou Ecwid je développe des sites Ecommerce de toutes tailles.</p>
				</div>
			</div>
			<div class="service">
				<div class="one-service">
					<div class="title">
						<img src="~/assets/img/Rectangle-47.png" alt="">
						<h3>Design</h3>
					</div>
					<p class="p-reg">Vous voulez un site web à votre image ? Je peux vous proposer mes services de designer graphique pour faire de vos idées une réalité.</p>
				</div>
				<div class="one-service">
					<div class="title">
						<img src="~/assets/img/Rectangle-47.png" alt="">
						<h3>Référencement, accessibilité & responsive</h3>
					</div>
					<p class="p-reg">Je suis particulièrement attentive au référencement naturel (SEO) de votre site, à son accessibilité par tou·te·s. Tous mes sites ont un design adaptable smartphone et tablette.</p>
				</div>
				<div class="one-service">
					<div class="title">
						<img src="~/assets/img/Rectangle-47.png" alt="">
						<h3>Conseil</h3>
					</div>
					<p class="p-reg">Et bien sûr, je peux vous proposer en plus mes services de designer graphique pour rendre vos idées plus belles !</p>
				</div>
			</div>
		</div>
  </div>
</template>

<style lang="scss" scoped>
.services-container {
  display: flex;
	flex-direction: column;
	align-items: center;
	margin: 70px 0;

  & .content {
    display: flex;
    width: 80vw;
    max-width: 860px;
    margin: 70px 0 35px 0;
    flex-direction: column;

    & .service-pres {
      border: 1px solid red;
      display: flex;
      margin: 20px 0;

      & img {
        width: 700px;
        margin: 0 20px 0 0;
      }
    }
  }

	& .services {
		// border: 2px solid green;
		display: flex;
		flex-direction: column;
		width: 95vw;
		max-width: 950px;
		margin: 70px 0;
		
		& .service {
			// border: 2px solid red;
			display: flex;
			justify-content: space-between;

			& .one-service {
				// border: 1px solid $light-brown;
				// background-color: $light-pink;
				// border-radius: 8px;
				width: 260px;
				padding: 20px;
				display: flex;
				flex-direction: column;
				align-items: center;
				margin: 20px 0;

				& .title {
					// border: 1px solid red;
					display: flex;
					flex-direction: column;
					align-items: center;
					margin: 0 0 20px 0;
          text-align: center;
				}

				& p {
					font-size: 16px;
				}
				
				& img {
					width: 90px;
					height: 90px;
					margin: 0 0 15px 0;
				}
			}

		}
	}
}
</style>
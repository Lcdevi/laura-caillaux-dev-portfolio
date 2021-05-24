<template>
	<div id="footer">
		<div>
			<NuxtLink to="/">Home</NuxtLink>
			<NuxtLink to="/about">About</NuxtLink>
			<NuxtLink to="/contact">Contact</NuxtLink>
			<NuxtLink to="/work">Work</NuxtLink>
		</div>
		<div>polices de caractère utilisées : Raleway & Quattrocento </div>
		<div>copyright Laura Caillaux 2021</div>
	</div>
</template>

<style lang="scss" scoped>
#footer {
	// border: 1px solid red;
	font-family: $ff-sans;
	font-size: 14px;
	display: flex;
	justify-content: space-between;
	align-items: center;
	padding: 0 20px 20px 20px;
	& a {
		margin-right: 10px;
	}
}
</style>

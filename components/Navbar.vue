<template>
	<div id="header">
		<div id="navbar">
			<div class="menu-link" :class="[isActive ? 'color' : 'invisible']">
				<NuxtLink to="/">Laura Caillaux</NuxtLink>
			</div>
			<div class="menu-link" v-on:click="togglemenu">
				<p id="menu"><span>M</span>enu</p>
			</div>
			<div class="menu-link" :class="[isActive ? 'color' : 'invisible']">
				<NuxtLink to="/about">About</NuxtLink>
			</div>
		</div>

		<div class="burger-menu"  :class="[isActive ? 'remove-menu' : 'display-menu']">
			<ul>
				<li v-on:click="togglemenu">
					<NuxtLink to="/">home</NuxtLink>
				</li>
				<li v-on:click="togglemenu">
					<NuxtLink to="/work">work</NuxtLink>
				</li>
				<li v-on:click="togglemenu">
					<NuxtLink to="/about">about</NuxtLink>
				</li>
				<li v-on:click="togglemenu">contact</li>
				<li v-on:click="togglemenu">credit</li>
			</ul>
		</div>
	</div>
</template>

<script>
export default {

	data: function () {
    return {
      isActive: true
    }
  },

	computed: {
		computedClass() {
			let className = 'remove-menu';

			return className;
		}
	},

	methods: {
    togglemenu: function () {

		this.isActive = !this.isActive
    
		}
  }
}
</script>

<style lang="scss" scoped>

#header {
	position: relative;

	#navbar {
		// border: 1px solid red;
		height: 130px;
		font-family: $ff-sans;
		font-size: 28px;
		display: flex;
		justify-content: space-between;
		align-items: center;

		& .menu-link {
			width: 120px;
			text-align: center;
		}

		& #menu {
			border-top: 1px solid $brown;
			border-bottom: 1px solid $brown;
			transform: rotate(340deg);
			padding: 6px 0;
			text-transform: uppercase;
			width: 100px;
		}

		& #menu:hover {
			padding: 8px 0;
		}

		.color {
			color: $brown;
		}

		.invisible {
			color: $pink;
		}
	}

	.burger-menu {
		// border: 1px solid red;
		position: absolute;
		width: 100%;
		// background-color: $pink;
		// background: linear-gradient($pink, rgba(255,245,219, 0.5));
background: linear-gradient(180deg, rgba(255,245,219,1) 0%, rgba(255,245,219,1) 40%, rgba(255,245,219,0.6923144257703081) 100%);
		z-index: 100;
		padding: 40px 0 140px 0;
		text-align: center;
		height: 100vh;

		& li {
			font-family: $ff-serif;
			text-transform: uppercase;
			font-size: 35px;
			margin: 20px 0;
		}
	}

	.display-menu {
		display: block;
	}

	.remove-menu {
		display: none;
	}

}





</style>

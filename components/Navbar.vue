<template>
	<div id="header">
		<div id="navbar">
			<div class="menu-link" :class="[isActive ? 'color' : 'invisible']">
				<NuxtLink to="/">Laura Caillaux</NuxtLink>
			</div>
			<div class="menu-link" v-on:click="togglemenu">
				<p id="menu" :class="[isActive ? 'display-menu' : 'remove-menu']"><span>M</span>enu</p>
				<div class="cross" :class="[isActive ? 'remove-menu' : 'display-menu']">
					<div class="line"></div>
				</div>
			</div>
			<div class="menu-link" :class="[isActive ? 'color' : 'invisible']">
				<NuxtLink to="/contact">Contact</NuxtLink>
			</div>
		</div>

		<div class="burger-menu" :class="[isActive ? 'remove-menu' : 'display-menu']">
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
				<li v-on:click="togglemenu">
					<NuxtLink to="/contact">contact</NuxtLink>
				</li>
				<li v-on:click="togglemenu">
					<NuxtLink to="/credit">credit</NuxtLink>
				</li>
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
		position: fixed;
		top: 0;
		width: 100%;
		height: 130px;
		font-family: $ff-sans;
		font-size: 28px;
		display: flex;
		justify-content: space-between;
		align-items: center;
		background-color: $pink;

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

		& .color {
			color: $brown;
		}

		& .invisible {
			color: $pink;
		}

		& .cross {
			position: relative;
			width: 50px;
			height: 50px;
			cursor: pointer;
			border: 1px solid $brown;
			margin: 35px;
			border-radius: 50%;

			&	.line {
				width: 50px;
				height: 1px;
				background-color: $brown;
				border-radius: 5px;
				transform: rotate(25deg) translate(9px, 22px);
			}

			&	.line::before,
				.line::after {
				content: '';
				position: absolute;
				width: 50px;
				height: 1px;
				background-color: $brown;
				border-radius: 5px;
				}
			&	.line::before {
				transform: translateX(-25px) rotate(116deg);
			}
			& .line::after {
				transform: translateX(-25px) rotate(55deg);
			}
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
		height: 140vh;

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

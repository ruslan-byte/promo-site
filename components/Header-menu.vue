<template>
	<div class="header-menu">
		<button class="header-menu__button" @click="toggleMenu">
			<BurgerLogo />
		</button>	
		<Popup ref="burger">
			<div class="header-menu__body" >
				<a href="#" class="header-menu__link">Умения</a>
				<a href="#" class="header-menu__link">Партфолио</a>
				<a href="#" class="header-menu__link">Связь со мной</a>
			</div>
		</Popup>
	</div>
</template>
<script>
import BurgerLogo from "~/assets/svg/burger.svg?inline";
export default {
	name: 'HeadeMenu',
	components:{BurgerLogo},
	methods:
	{
		toggleMenu()
		{
			this.$refs.burger.toggle();
		}
	}
}
</script>
<style>
	
</style>

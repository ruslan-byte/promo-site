<template>
	<div class="header-menu">
		<div class="header-menu__content header-menu__content--mobile">
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
		<div class="header-menu__content header-menu__content--desktop">
			<a href="#" class="header-menu__link">Умения</a>
			<a href="#" class="header-menu__link">Партфолио</a>
			<a href="#" class="header-menu__link header-menu__link--contact">Связь со мной</a>
		</div>
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
<style lang="scss">
	.header-menu__body
	{
		display: flex;
		flex-direction: column;
		align-items: flex-start;
	}
	.header-menu__link
	{
		display: inline-block;
		line-height: 30px;
	}
	.header-menu__button
	{
		background: none;
		border: none;
	}
	.header-menu__content--desktop{display: none;}
	@media (min-width: 768px)
	{
		.header-menu__content--desktop
		{
			display: block;
			font-size: 0;
		}
		.header-menu__content--mobile{display: none}
		.header-menu__link
		{
			display: inline-block;
			padding: 32px 24px;
			line-height: 16px;
			&:hover
			{
				background: #5221E6;
			}
		}

	}
</style>

<template>
	<header class="header container">
		<div class="header__logo"><LogoSvg/></div>
		<HeaderMenu class="header__menu" />
	</header>
</template>
<script>
import LogoSvg from '~/assets/svg/logo.svg?inline'
export default {
	components: { LogoSvg },
	name: 'Header'
}
</script>
<style lang="scss">
	.header
	{
		display: flex;
		justify-content: space-between;
		padding-top: 24px;
		padding-bottom: 24px;
	}
	.header__logo{font-size: 0}
	.header__logo svg
	{
		height: 20px;
		width: 25px;
		fill: var(--white)
	}
	@media (min-width: 768px)
	{
		.header
		{
			align-items: center;
			padding: 0;			
		}
		.header__logo svg
		{
			width: 50px;
			height: 50px;
		}
	}
</style>
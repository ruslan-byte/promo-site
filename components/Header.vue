<template>
	<header class="header">
		<div class="header__logo">Logo</div>
		<HeaderMenu class="header__menu" />
	</header>
</template>
<script>
export default {
  name: 'Header'
}
</script>
<style lang="scss">
	.header
	{
		display: flex;
		justify-content: space-between;
	}
</style>
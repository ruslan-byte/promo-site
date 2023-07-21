<template>
	<div class="header-menu">
		<button class="header-menu__button" @click="toggleMenu">
			<svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
				<rect width="24" height="24"/>
				<rect x="3" y="6" width="18" height="3" fill="#C4C4C4"/>
				<rect x="8" y="14" width="13" height="3" fill="#C4C4C4"/>
			</svg>
		</button>	
		<div class="header-menu__body" v-if="isMenuOpen">
			<a href="#" class="header-menu__link">Умения</a>
			<a href="#" class="header-menu__link">Партфолио</a>
			<a href="#" class="header-menu__link">Связь со мной</a>
		</div>
	</div>
</template>
<script>
export default {
  name: 'HeadeMenu',
  data () {
  	return {
  		isMenuOpen:false,
  	}
  },
  methods: {
  	toggleMenu() 
  	{
  		this.isMenuOpen = !this.isMenuOpen;
  	}
  }
}
</script>
<template>
	<Transition>
		<div class="popup" v-if="isOpen">
			<div class="popup__content">
				<button class="popup__cross"  @click="close">
					<CrossLogo></CrossLogo>
				</button>
				<slot></slot>
			</div>
			<div class="popup__background" @click="close"></div>
		</div>
	</Transition>
</template>
<script>
import CrossLogo from "~/assets/svg/cross.svg?inline";
export default {
	components:{CrossLogo},
	data() 
	{
		return { isOpen: false }
	},
	methods:
	{
		toggle()
		{
			this.isOpen = !this.isOpen;
		},
		close()
		{
			this.isOpen = false;
		}
	}
}
</script>

<style lang="scss">
	.popup
	{
		position: fixed;
		top: 0;
		bottom: 0;
		right: 0;
		left: 0;
	}
	.popup__background
	{
		position: absolute;
		left: 0;
		top: 0;
		bottom: 0;
		right: 0;
		background: rgba(0,0,0,0.2);
	}
	.popup__content
	{
		position: absolute;
		left: 20px;
		right: 20px;
		bottom: 20px;
		top: 20px;
		background: var(--second-bg-color);
		border-radius: 20px;
		z-index: 2;
		padding: 38px 18px 12px 18px;
		overflow: auto; 
	}
	.popup__cross
	{
		position: absolute;
		right: 16px;
		top: 16px;
		border:none;
		width: 24px;
		height: 24px;
		background: none;
		padding: 0;
		svg
		{
			stroke:var(--white);
			width: 24px;
			height: 24px;
		}
	}
	.v-enter-active,
	.v-leave-active {
	  transition: opacity 0.3s ease;
	}

	.v-enter-from,
	.v-leave-to {
	  opacity: 0;
	}
</style>
<template>
	<header class="header">
		<div class="container">
			<div class="header__box">
				<router-link to="/" class="header__logo logo">
						<img src="../assets/img/logo.png" alt="">
				</router-link>
				
				<div class="header__controls">
					<button class="btn btn__primary">
						<img src="../assets/img/icons/user.svg" alt="user">
						Войти
					</button>
					<button class="btn btn__outline" @click="openModal">
						<img src="../assets/img/icons/cart.svg" alt="cart">
						Корзина
					</button>
				</div>
				</div>
		</div>
	  		</header>
</template>

<script setup>
const emit = defineEmits(['toggleModal'])
const openModal = () => emit('toggleModal')
	
</script>

<style scoped>
.header {
	min-height: 124px;
	display: flex;
	align-items: center;


}
.header__box {
	height: 100%;
	display: flex;
	align-items: center;
	justify-content: space-between;

}
.header__controls {
	display: flex;
	align-items: center;
	justify-content: flex-end;
	gap: 8px;
}

</style>
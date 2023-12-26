<template>
	<footer class="footer">
		<div class="container">
			<div class="footer__box">
				<router-link to="/" class="footer__logo logo">
						<img src="../assets/img/logo.png" alt="logo">
				</router-link>
				<div class="footer__nav">
					<ul>
						<li>Ресторанам </li>
						<li>Курьерам</li>
						<li>Пресс-центр</li>
						<li>Контакты</li>
					</ul>
				</div>
				<div class="footer__social">
					<img src="../assets/img/social/instagram.svg" alt="inst">
					<img src="../assets/img/social/fb.svg" alt="fb">
					<img src="../assets/img/social/vk.svg" alt="vk">
				</div>
			</div>
		</div>
	</footer>
</template>

<script>
export default {

}
</script>

<style scoped>
	.footer {
	min-height: 156px;
	display: flex;
	align-items: center;
	padding: 60px 0;
}
.footer__box {
	height: 100%;
	display: flex;
	align-items: center;
	justify-content: space-between;
	gap: 36px;
	flex-wrap: wrap;
}
.footer__nav {
	flex-grow: 1;
}
.footer__nav ul {
	display: flex;
	align-items: center;
	list-style-type: none;
	margin: 0;
	padding: 0;
	gap: 15px;
	flex-wrap: wrap;

}
.footer__nav ul li {
	font-size: 18px;
	font-weight: 400;
	
}
.footer__social {
	display: flex;
	align-items: center;
	justify-content: flex-end;
	gap: 20px;
}

</style>
<template>
	<div class="cart-modal__overlay" :class="{open: isOpen}" @click.self="closeModal()">
      <div class="cart-modal">
        <div class="cart-modal__header">
          <div class="cart-modal__header_title">Корзина</div>
          <span class="cart-modal__header_close">
            <img src="../assets/img/icons/close.svg" alt="close" @click="closeModal()">
          </span>
        </div>
        <div class="cart-modal__body">
          <div class="cart-item">
            <p class="cart-item__title">Ролл угорь стандарт</p>

            <div class="cart-item__controls">
              <div class="cart-item__controls_price"> 250 ₽ </div>

              <button class="btn btn__outline">-</button>
              <div class="cart-item__controls_count">1</div>
              <button class="btn btn__outline">+</button>
            </div>
          </div>
          <div class="cart-item">
            <p class="cart-item__title">Ролл угорь стандарт</p>

            <div class="cart-item__controls">
              <div class="cart-item__controls_price"> 250 ₽ </div>

              <button class="btn btn__outline">-</button>
              <div class="cart-item__controls_count">1</div>
              <button class="btn btn__outline">+</button>
            </div>
          </div>
          <div class="cart-item">
            <p class="cart-item__title">Ролл угорь стандарт</p>

            <div class="cart-item__controls">
              <div class="cart-item__controls_price"> 250 ₽ </div>

              <button class="btn btn__outline">-</button>
              <div class="cart-item__controls_count">1</div>
              <button class="btn btn__outline">+</button>
            </div>
          </div>
          <div class="cart-item">
            <p class="cart-item__title">Ролл угорь стандарт</p>

            <div class="cart-item__controls">
              <div class="cart-item__controls_price"> 250 ₽ </div>

              <button class="btn btn__outline">-</button>
              <div class="cart-item__controls_count">1</div>
              <button class="btn btn__outline">+</button>
            </div>
          </div>
          <div class="cart-item">
            <p class="cart-item__title">Ролл угорь стандарт</p>

            <div class="cart-item__controls">
              <div class="cart-item__controls_price"> 250 ₽ </div>

              <button class="btn btn__outline">-</button>
              <div class="cart-item__controls_count">1</div>
              <button class="btn btn__outline">+</button>
            </div>
          </div>
        </div>
        <div class="cart-modal__footer">
          <div class="cart-modal__footer_price">1250 ₽</div>
          <div class="cart-modal__footer_controls">
            <button class="btn btn__primary">
              Оформить заказ
            </button>
            <button class="btn btn__outline">
              Отмена
            </button>
          </div>

        </div>
      </div>
    </div>
</template>

<script setup>
const { isOpen } = defineProps({ isOpen: Boolean })
const emit = defineEmits(['toggleModal'])
const closeModal = () => emit('toggleModal')

</script>

<style scoped>
	.cart-modal__overlay {
	display: none;
	position: fixed;
	top: 0;
	bottom: 0;
	right: 0;
	left: 0;
	background: rgba(0, 0, 0, 0.40);
	align-items: center;
	justify-content: center;
}
.cart-modal__overlay.open {
	display: flex;
}
.cart-modal {
	width: 100%;
	max-width: 870px;
	padding: 40px 45px;
	background-color: #fff;
	border-radius: 8px;
}
.cart-modal__header {
	display: flex;
	align-items: center;
	justify-content: space-between;
	margin-bottom: 48px;
}
.cart-modal__header_title {
	font-size: 36px;
	font-weight: 700;
	margin: 0;
}
.cart-modal__header_close {
	cursor: pointer;
}
.cart-modal__footer {
	display: flex;
	align-items: center;
	justify-content: space-between;
	flex-wrap: wrap;
	/*gap: 15px;*/
	margin-top: 50px;
}

.cart-modal__footer_price {
	border-radius: 5px;
	background: #262626;
	color: #fafafa;
	font-size: 20px;
	font-weight: 700;
	padding: 15px 20px;
}
.cart-modal__footer_controls {
	display: flex;
	align-items: center;
	gap: 10px;
}
.cart-item {
	display: flex;
	align-items: center;
	justify-content: space-between;
	flex-wrap: wrap;
	gap: 10px;
}
.cart-item:not(:last-child) {
	padding-bottom: 10px;
	margin-bottom: 10px;
	border-bottom: 1px solid #d9d9d9;
}
.cart-item__title {
	color: #000;
	font-size: 18px;
	font-weight: 400;
	line-height: 32px;
	margin: 0;
}
.cart-item__controls {
	display: flex;
	align-items: center;
}

.cart-item__controls_price {
	margin-right: 47px;
	display: flex;
	align-items: center;
	color: #000;
	font-size: 20px;
	font-weight: 700;
	line-height: 32px;
}
.cart-item__controls button{
	border: 1px solid #40a9ff;
	color: #40a9ff;
}

.cart-item__controls_count {
	margin: 0 15px;
}

</style>
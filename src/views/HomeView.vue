<template>
  <section class="banner">
    <div class="container">
      <div class="banner-item">
        <h2 class="banner-item__title">
          Онлайн-сервис<br />
          доставки еды на дом
        </h2>
        <p class="banner-item__subtitle">
          Блюда из любимого ресторана привезет курьер в перчатках, маске и с
          антисептиком
        </p>
      </div>
    </div>
  </section>
  <section class="products">
    <div class="container">
      <div class="products-header">
        <h3 class="products-header__title">Рестораны</h3>
        <input
          type="text"
          class="products-header__search"
          placeholder="Поиск блюд и ресторанов"
        />
      </div>
      <div class="products__wrapper" id="rests-container">
        <router-link
          
          class="products-card"
          v-for="rest in restArrey"
          :key="rest.id"
					:to="`/rest?id=${rest.id}`"
        >
          <div class="products-card__image">
            <img :src="getUrl(rest.image)" alt="rest" />
          </div>
          <div class="products-card__description">
            <div class="products-card__description-row">
              <h4 class="products-card__description_title">{{  rest.title }}</h4>
              <div class="products-card__description_bage">{{  rest.time }}</div>
            </div>
            <div class="products-card__description-row">
              <div class="products-card__description-info">
                <div class="products-card__description-info_rating">
                  <img src="../assets/img/star.svg" alt="star" />
                  {{  rest.rating }}
                </div>
                <div class="products-card__description-info_price">
                  {{  rest.price }}
                </div>
                <div class="products-card__description-info_groop">{{  rest.type }}</div>
              </div>
            </div>
          </div>
        </router-link>
        
      </div>
    </div>
  </section>
</template>

<script setup>
import {restArrey} from '../constants/rests'
const getUrl = (name) => {
	return new URL(`../assets/img/rests/${name}`, import.meta.url)
	//`../assets/images/rests/rest-1.jpg`
}

</script>

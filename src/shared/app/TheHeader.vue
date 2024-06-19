<template>
  <header class="header">
    <div class="container header__container">
      <img src="@/assets/img/logo.png" alt="Logo" />
      <nav class="header__nav" :class="{ 'header__nav--opened': isMenuOpen }">
        <button class="header__close" @click="isMenuOpen = false">
          <span></span>
          <span></span>
        </button>
        <ul class="header__nav-list">
          <li>
            <a class="header__nav-link" href="#">Home</a>
          </li>
          <li>
            <a class="header__nav-link" href="#">O mnie</a>
          </li>
          <li>
            <a class="header__nav-link" href="#">Kurs</a>
          </li>
        </ul>
      </nav>
      <button class="header__burger" @click="isMenuOpen = true">
        <span></span>
        <span></span>
        <span></span>
      </button>
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue';

const isMenuOpen = ref(false);
</script>

<style scoped lang="scss">
.header {
  font-family: var(--secondary-font);

  &__container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 20px;

    @include breakpoint($screen-lg) {
      padding: 30px 60px;
    }
  }

  &__nav {
    margin-left: auto;
    position: fixed;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 20;
    width: var(--breakpoint-sm);
    transform: translateY(-100%);
    background: var(--primary-color);
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    transition: transform 0.4s var(--timing-function);

    @include breakpoint($screen-lg) {
      position: static;
      transform: none;
      background: none;
    }

    &--opened {
      transform: translateY(0);
    }
  }

  &__nav-list {
    display: flex;
    flex-direction: column;
    gap: 60px;

    @include breakpoint($screen-lg) {
      flex-direction: row;
      gap: 90px;
    }
  }

  &__nav-link {
    font-size: 20px;
    transition: color 250ms var(--timing-function);

    &:hover {
      color: var(--hover-color);
    }
  }

  &__burger {
    cursor: pointer;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    background: none;
    border: 0;
    padding: 10px;
    width: 45px;
    height: 40px;

    @include breakpoint($screen-lg) {
      display: none;
    }

    span {
      background: var(--secondary-color);
      height: 2px;
      width: 100%;
    }
  }

  &__close {
    position: absolute;
    top: 45px;
    right: 28px;
    width: 30px;
    height: 30px;
    cursor: pointer;
    background: none;
    border: 0;

    @include breakpoint($screen-lg) {
      display: none;
    }

    span {
      background: var(--secondary-color);
      height: 2px;
      position: absolute;
      top: 50%;
      right: 0;
      left: 0;
      transform-origin: center;
      transition: transform 0.4s var(--timing-function);

      &:first-child {
        transform: translateY(-50%) rotate(45deg);
      }

      &:last-child {
        transform: translateY(-50%) rotate(-45deg);
      }
    }
  }
}
</style>

<template>
  <header class="header">
    <div class="container header__container">
      <img src="@/assets/img/logo.png" alt="Logo" />
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
    </div>
  </header>
</template>

<style scoped lang="scss">
.header {
  font-family: var(--secondary-font);

  &__container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 30px 60px;
  }

  &__nav-list {
    display: flex;
    gap: 60px;

    @include breakpoint($screen-lg) {
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
}
</style>

<template>
  <header class="header">
    <div class="container header-container">
      <img src="@/assets/logo.png" alt="Logo" class="logo" />
      <ul class="header_nav-list">
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

<style scoped>
.header {
  font-family: var(--secondary-font);
}

.header-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 20px;
}

.header_nav-list {
  display: flex;
  gap: 90px;

  list-style: none;
  margin: 0;
  padding: 0;
  line-height: 22px;
}

.header__nav-link {
  font-size: 20px;
  transition: color 250ms var(--timing-function);
}

.header__nav-link:hover {
  color: var(--hover-color);
}
</style>

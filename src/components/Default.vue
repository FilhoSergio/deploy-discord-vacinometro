<template>
  <div>
    <div class="layout">
      <header class="header">
        <strong>
          <img src="@/assets/logo_locadora.svg" width="40" height="40" />
          <a class="logo-link" to="/">Vacinômetro</a>
        </strong>
        <nav class="nav">
          <a class="nav__link" href="/">Início</a>
          <a class="nav__link" href="/about/">Sobre</a>
          <a class="nav__link" href="/dados/">Dados</a>
        </nav>
      </header>
      <slot />
    </div>
    <div class="footer"></div>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
body {
  font-family: -apple-system, system-ui, BlinkMacSystemFont, "Segoe UI", Roboto,
    "Helvetica Neue", Arial, sans-serif;
  margin: 0;
  padding: 0;
  line-height: 1.5;
}

.layout {
  max-width: 760px;
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
  height: 80px;
}

.nav__link {
  margin-left: 20px;
  text-decoration: none;
  color: #1eb19e;
  cursor: pointer;
}

.logo-link {
  text-decoration: none;
  color: #1eb19e;
}

.footer {
  width: 100%;
  height: 400px;
  background: #1eb19e;
  color: #ffffff;
  bottom: 0;
  display: none;
}
</style>

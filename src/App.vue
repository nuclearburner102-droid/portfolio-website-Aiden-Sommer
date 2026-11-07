<script setup lang="ts">
</script>

<template>
  <div class="app">
    <header class="site-header">
      <div class="header-inner">
        <RouterLink to="/" class="logo">Aiden Sommer</RouterLink>
        <nav class="nav">
          <RouterLink to="/" class="nav-link">Home</RouterLink>
          <RouterLink to="/about" class="nav-link">About</RouterLink>
          <RouterLink to="/portfolio" class="nav-link">Portfolio</RouterLink>
        </nav>
      </div>
    </header>

    <RouterView />
  </div>
</template>

<style scoped>
.app {
  font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.site-header {
  background: #ffffff;
  border-bottom: 1px solid #e5e7eb;
  position: sticky;
  top: 0;
  z-index: 100;
}

.header-inner {
  max-width: 1100px;
  margin: 0 auto;
  padding: 0.9rem 1.5rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1.5rem;
}

.logo {
  text-decoration: none;
  font-weight: 700;
  font-size: 1.15rem;
  color: #111;
}

.nav {
  display: flex;
  gap: 0.25rem;
}

.nav-link {
  text-decoration: none;
  padding: 0.45rem 0.9rem;
  border-radius: 8px;
  font-size: 0.95rem;
  font-weight: 500;
  color: #444;
}

.nav-link:hover {
  background: #f1f5f9;
  color: #216adf;
}

.nav-link.router-link-active {
  background: #eff6ff;
  color: #1e40af;
  font-weight: 600;
}
</style>
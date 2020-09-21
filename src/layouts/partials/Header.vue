<template>
  <div>
    <header class="layout-header">
      <nav class="nav">
        <g-link to="/" class="logo"><img src="../../favicon.png" width="22" height="22"></g-link>
        <div class="toggle-theme"><ToggleTheme /></div>
      </nav>
    </header>
  </div>
</template>

<script>
import ToggleTheme from "@/components/ToggleTheme";
export default {
  components: {
    ToggleTheme,
  },
};
</script>

<style>
  .layout-header {
    position: fixed;
    top: 0;
    left: 0;
    margin: auto;
    width: 100%;
  }
  .nav {
    justify-content: space-between;
    padding: 5px;
    display: flex;
    align-items: center;
    margin: 0px 68px;
  }
  .logo {
    padding: 5px;
  }
  .toggle-theme {
    padding: 5px;
  }
</style>
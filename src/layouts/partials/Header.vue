<template>
  <div>
    <header class="layout-header">
      <nav class="nav">
        <div class="logo">LOGO</div>
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
    border: 1px solid rgb(111,41,97);
    padding: 5px;
    display: flex;
    align-items: center;
  }
  .logo {
    padding: 5px;
    border: 1px solid rgba(111,41,97,.5);
    border-radius: .5em;
  }
  .toggle-theme {
    padding: 5px;
    border: 1px solid rgba(111,41,97,.5);
    border-radius: .5em;
  }
</style>
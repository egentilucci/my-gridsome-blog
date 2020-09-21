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
    border: 1px solid rgb(111,41,97);
    border-radius: .5em;
  }
  .nav {
    justify-content: space-between;
    padding: 5px;
    display: flex;
    align-items: center;
    margin: 0px 68px;
    border: 1px solid rgb(111,41,97);
    border-radius: .5em;
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
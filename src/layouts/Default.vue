<template>

  <main class="check-border" role="main">
  
    <div><Header /></div>
    
    <div class="outer-layout">

      <div class="item-side left check-border"><LeftSidebar /></div>
      
      <div class="inner-layout check-border">
        <div class="item-center"><slot /></div> <!-- Page/Template will be inserted here -->
      </div>
      
      <div class="item-side right check-border"><RightSidebar /></div>

    </div>

    <div><Footer /></div>
  
  </main>
  
</template>

<script>
  import Header from "./partials/Header";
  import LeftSidebar from "./partials/LeftSidebar";
  import RightSidebar from "./partials/RightSidebar";
  import Footer from "./partials/Footer";

  export default {
    components: {
      Header,
      LeftSidebar,
      RightSidebar,
      Footer
    }
  };
</script>

<style>
  :root {
    --text-color: #333;
    --border-color: #fecd43;
    --bkg-color: white;
    --line-color: #cdc8c5;
  }
  :root [data-theme="sepia"] {
    --text-color: #433422;
    --border-color: #00a672;
    --bkg-color: #f1e7d0;
    --line-color: #00a672;
  }
  :root [data-theme="dark"] {
    --text-color: #ffffff;
    --border-color: #fecd43;
    --bkg-color: #030200;
    --line-color: #fecd43;
  }
  body {
    font-family: -apple-system, system-ui, BlinkMacSystemFont, "Segoe UI", Roboto,
      "Helvetica Neue", Arial, sans-serif;
    margin: 0;
    padding: 0;
    line-height: 1.5;
    /* border: 15px solid var(--border-color); */
    min-height: 100vh;
    background-color: var(--bkg-color);
    color: var(--text-color);
    transition: background 0.5s;
  }
  .outer-layout {
    display: flex;
    align-items: center;
  }
  .inner-layout {
    max-width: 768px;
    margin: 0 auto;
    padding-left: 20px;
    padding-right: 20px;
    display: flex;
  }
  .item-side {
    height: 400px;
    width: 100px;
    text-align: center;
    vertical-align: middle;
  }
  .left {
    margin-left: 68px;
  }
  .right {
    margin-right: 68px;
  }
  .item-center {
    flex-grow: 1;
    padding-bottom: 50px;
  }
  .link {
    border: 2px solid var(--border-color);
    padding: 5px;
    color: var(--text-color);
    text-decoration: none;
  }
  .check-border {
    border: 1px solid rgba(111,41,97,.5);
    border-radius: .5em;
  }
</style>

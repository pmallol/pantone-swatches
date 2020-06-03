<template>
  <div id="app">
    <div class=header>
      <h1>PANTONE <span>swatches</span></h1>
      <div id="nav">
        <router-link to="/">Home</router-link>
        <router-link to="/about">About</router-link>
      </div>
    </div>
    <router-view/>
    <div class=footer>
      <p>PANTONE colors thanks to <a href="https://github.com/vanderlee/colorpicker/wiki/Pantone-colors-(csv,-semicolon-separated)" target="_blank">@vanderlee</a></p>
    </div>
  </div>
</template>

<style>
  #app {
    font-family: Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #000000;
    max-width: 80vw;
    height: 100vh;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
  }

  .header {
    margin: 3rem 0;
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
  }

  .header h1 {
    font-size: 2.5rem;
    font-weight: bold;
    display: inline-flex;
    flex-direction: column;
  }

  .header h1:hover {
    color: transparent;
    background-clip: text;
    background-image: linear-gradient(to left, violet, indigo, blue, green, yellow, orange, red);
    cursor: default;
  }

  .header h1 span {
    letter-spacing: 1px;
    font-size: 1.5rem;
    font-weight: normal;
  }

  #nav a {
    font-weight: bold;
    color: #444444;
    text-decoration: none;
    margin: 0 1rem;
  }

  .footer {
    font-size: .8rem;
    padding: 2rem 0;
    margin: 2rem 0;
    margin-top:auto;
  }

  .footer a {
    color: black;
    text-decoration: none;
  }

  #nav a:hover,
  #nav a.router-link-exact-active,
  .footer a:hover {
    color: #6945a9;
  }
</style>

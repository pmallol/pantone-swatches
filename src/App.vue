<template>
  <div id="app">
    <header>
      <h1>PANTONE <span>swatches</span></h1>
      <div id="nav">
        <router-link to="/">Home</router-link>
        <router-link to="/about">About</router-link>
      </div>
    </header>
    <main>
      <router-view/>
    </main>
    <footer>
      <p><b>PANTONE</b> colors codes thanks to <a href="https://github.com/vanderlee/colorpicker/wiki/Pantone-colors-(csv,-semicolon-separated)" target="_blank">@vanderlee</a></p>
    </footer>
  </div>
</template>

<style>
#app {
  background-color: #f7f7f7;
  font-family: Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #000000;
  max-width: 100vw;
  min-height: 100vh;
  height: 100%;
  margin: 0 auto;
}

#app > * {
  max-width: 80vw;
  margin-left: auto;
  margin-right: auto;
}

header {
  padding: 3rem 0;
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
}

header h1 {
  font-size: 2.5rem;
  font-weight: bold;
  display: inline-flex;
  flex-direction: column;
}

header h1:hover {
  color: transparent;
  background-clip: text;
  background-image: linear-gradient(to left, violet, indigo, blue, green, yellow, orange, red);
  cursor: default;
}

header h1:hover span {
  color: #000000;
}

header h1 span {
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

main {
  min-height: calc(100vh - 23rem);
}

footer {
  font-size: .8rem;
  text-align: center;
  padding: 8rem 0 2rem;
  height: calc(11 * 1rem);
}

footer a {
  color: black;
  text-decoration: none;
}

#nav a:hover,
#nav a.router-link-exact-active,
footer a:hover {
  color: #f93a2b;
}
</style>

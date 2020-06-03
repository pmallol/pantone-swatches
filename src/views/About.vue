<template>
  <div class="about">
    <h1>Hola,</h1>
    <h2>Thanks for stopping by :)</h2>
    <p>This is still a work in progress.</p>
    <div class="contact"><a href="https://about.tokto.dev">Get in touch!</a></div>
  </div>
</template>

<style scoped>
h1 {
  font-size: 2rem;
  font-weight: bold;
  margin: 1rem 0;
}

.contact a {
  color: #000000;
  font-weight: bold;
  text-decoration: none;
  display: inline-block;
  position: relative;
  z-index: 1;
}

.contact a:hover { color: inherit }

.contact a:hover::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: 0;
  height: .1rem;
  width: 100%;
  background: linear-gradient(to left, violet, indigo, blue, green, yellow, orange, red);
  z-index: -1;
}

p { margin: 1rem 0;}
</style>
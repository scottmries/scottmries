<template>
  <div class="flex">
    <nav class="main-nav">
      <div></div>
      <ul>
        <li><nuxt-link to="/">Home</nuxt-link></li>
        <li><nuxt-link to="/work">Work</nuxt-link></li>
        <li><nuxt-link to="/art">Art</nuxt-link></li>
        <!-- <li><nuxt-link to="life">Life</nuxt-link></li> -->
      </ul>
      <div></div>
    </nav>
    <main class="w-4/5">
      <Nuxt />
    </main>
  </div>
</template>

<style>
.main-nav {
  @apply .w-1/5 .flex .items-center;
  flex-direction: column;
}
.main-nav div, .main-nav ul li a {
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, rgba(101,0,105,1) 0%, black 50%, rgba(101,0,105,1) 100%);
  background-size: 400% 100%;
  animation: gradientMotion 45s ease infinite alternate;
  display: block;
}
.main-nav ul li a {
  padding: 0.5rem;
}
.main-nav ul {
  width: 100%;
}
main {
  @apply .p-4;
}
body {
  color: white;
  background: black;
  background: linear-gradient(90deg, black 0%,rgba(101,0,105,1) 50%, black 100%);
  background-size: 400% 100%;
  animation: gradientMotion 45s ease infinite alternate;
}
.main-nav ul li a.nuxt-link-exact-active {
  background: transparent;
  color: white;
}
@keyframes gradientMotion {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  align-items: center;
}
html {
  font-family:
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}


</style>

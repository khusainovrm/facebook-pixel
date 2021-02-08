<template>
  <div class="container">
    <div>
      <Logo />
      <h1 class="title">fb-pixel</h1>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          rel="noopener noreferrer"
          class="button--green"
        >
          Documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          rel="noopener noreferrer"
          class="button--grey"
        >
          GitHub
        </a>
      </div>
      <div class="box">1</div>
      <div class="box">2</div>
      <div class="box">3</div>
      <div @click="handler"><button>ACTION</button></div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    handler() {
      console.log('tadaa!')
    },
  },
}
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/

button {
  @apply py-2 px-4 bg-teal-900 text-white outline-none transition duration-200 ease-in-out transition-transform;

  &:focus {
    @apply outline-none shadow;
  }

  &:hover {
    @apply outline-none shadow bg-teal-700;
  }

  &:active {
    @apply shadow-xl bg-teal-600;
  }
}

.box {
  @apply mb-2 h-20 grid items-center bg-teal-300;
}

.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>

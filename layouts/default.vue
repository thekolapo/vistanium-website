<template>
  <div class="app">
    <Header />
    <Nuxt />
    <Footer />
  </div>
</template>

<style lang="scss">
@import '~/assets/scss/main.scss';

.app {
  padding: 4.3rem 5rem;

  @include screen('small') {
    padding-top: 3.2rem;
    padding-bottom: 3.6rem;
  }
}
</style>

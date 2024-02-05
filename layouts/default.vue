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
    padding: 3.6rem 2.5rem;
  }
}
</style>

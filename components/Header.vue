<template>
  <header class="header">
    <p>
      We’re a creative powerhouse at the intersection of media and technology.
      We craft compelling stories and products that resonate with audiences and
      drive action. ver excellence.
    </p>
    <p>
      We excel in bringing ambitious visions to life with our creative
      storytelling in video, audio, and text, and strategic solutions for
      exceptional brands.
    </p>
    <div class="header__links">
      <nuxt-link to="/">Home</nuxt-link>
      <nuxt-link to="/team">The team</nuxt-link>
    </div>
  </header>
</template>

<style lang="scss" scoped>
.header {
  display: flex;
  justify-content: space-between;

  > * {
    width: 30%;
  }

  &__links {
    text-align: right;

    a {
      color: #009a46;
    }

    a:not(:last-child) {
      margin-right: 2.4rem;
    }
  }
}
</style>

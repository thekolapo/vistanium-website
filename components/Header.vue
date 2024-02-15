<template>
  <header class="header">
    <p>
      We’re a creative powerhouse at the intersection of media and technology.
      We craft compelling stories and products that resonate with audiences and
      drive action.
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
  margin-bottom: 20rem;

  @include screen(med) {
    flex-wrap: wrap;

    p:not(:last-child) {
      margin-top: 1.6rem;
    }
  }

  @include screen(med) {
    margin-bottom: 10rem;
  }

  > * {
    width: 30%;

    @include screen(med) {
      width: 100%;
      order: 2;
    }
  }

  &__links {
    text-align: right;

    @include screen(med) {
      order: 1;
      margin-bottom: 2rem;
    }

    a {
      color: #009a46;
    }

    a:not(:last-child) {
      margin-right: 2.4rem;
    }
  }
}
</style>

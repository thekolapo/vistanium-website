<template>
  <div class="team"></div>
</template>

<script>
export default {
  data() {
    return {
      flickityOptions: {
        initialIndex: 1,
        prevNextButtons: false,
        pageDots: false,
        wrapAround: true,
        autoPlay: 3000,
      },
    }
  },
  mounted() {},
  methods: {},
}
</script>

<style lang="scss" scoped>
.home {
  margin-top: 20rem;

  &__projects {
    position: relative;
    width: 100vw;
    left: calc(-50vw + 50%);
    margin-top: 5.2rem;
  }

  &__project {
    width: 25%;
    margin-right: 5rem;

    img {
      height: 40rem;
      background: rgb(220, 220, 220);
      object-fit: cover;
      border: 1px solid #000000;
      border-radius: 30px;
    }

    .u-font-normal {
      margin: 3rem 0 1rem;
    }
  }

  &__collaborations {
    margin-top: 26rem;

    &-subtext {
      max-width: 90rem;
      text-align: center;
      margin: 0 auto;
    }

    &-brands {
      display: flex;
      margin: 7rem auto 0;
      width: fit-content;

      img:not(:last-child) {
        margin-right: 5rem;
      }
    }
  }
}
</style>

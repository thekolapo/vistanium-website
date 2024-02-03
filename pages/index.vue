<template>
  <div class="home">
    <div class="home__heading">
      <h1 class="u-font-h1">Our</h1>
      <h1 class="u-font-h1">Projects</h1>
    </div>
    <flickity ref="flickity" class="home__projects" :options="flickityOptions">
      <div class="home__project">
        <img src="@/assets/images/vistanium-mag-img.jpg" alt="" />
        <p class="u-font-normal">Vistanium Mag</p>
        <p>
          Immersive essays that narrate extraordinary true stories. They provide
          compelling insights into life in various cities, offering readers a
          rich, multifaceted perspective.
        </p>
      </div>
      <div class="home__project">
        <img src="@/assets/images/vistanium-mag-img.jpg" alt="" />
        <p class="u-font-normal">I too sabi</p>
        <p>
          A Nigeria-focused conversational "ask me anything" podcast that
          answers a wide range of questions through research and expert
          insights.
        </p>
      </div>
      <div class="home__project">
        <img src="@/assets/images/vistanium-mag-img.jpg" alt="" />
        <p class="u-font-normal">Sun and Country</p>
        <p>
          A story-led guide to understanding the Nigerian Civil War, capturing
          the events that led to it, how it played out on all sides, and how it
          continues to shape our world today.
        </p>
      </div>
      <div class="home__project">
        <img src="@/assets/images/vistanium-mag-img.jpg" alt="" />
        <p class="u-font-normal">I like girls</p>
        <p>
          A documentary-style, narrative-driven podcast exploring the diverse
          stories of African women. It offers firsthand insights into how gender
          shapes women's lives.
        </p>
      </div>
      <div class="home__project">
        <img src="@/assets/images/vistanium-mag-img.jpg" alt="" />
        <p class="u-font-normal">Vistanium Mag</p>
        <p>
          Immersive essays that narrate extraordinary true stories. They provide
          compelling insights into life in various cities, offering readers a
          rich, multifaceted perspective.
        </p>
      </div>
    </flickity>
    <div class="home__collaborations">
      <p class="u-font-normal home__collaborations-subtext">
        We collaborate with ambitious brands to advance their business
        objectives by offering strategic solutions in branding, product
        development, and marketing. Our services include strategy and content
        development, identity design, product strategy, marketing, and brand
        communications.
      </p>
      <div class="home__collaborations-brands">
        <img src="@/assets/images/lemfi.svg" alt="lemfi logo" />
        <img src="@/assets/images/flutterwave.svg" alt="flutterwave logo" />
        <img src="@/assets/images/rise.svg" alt="rise logo" />
        <img src="@/assets/images/archiving.svg" alt="archiving logo" />
        <img src="@/assets/images/piggyvest.svg" alt="piggyvest logo" />
        <img src="@/assets/images/mira.svg" alt="mira logo" />
      </div>
    </div>
  </div>
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

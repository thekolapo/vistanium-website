<template>
  <div class="home">
    <div class="home__header">
      <div class="home__header-heading">
        <h1 class="u-font-h1">Our</h1>
        <h1 class="u-font-h1">Projects</h1>
      </div>
      <div class="home__header-nav">
        <button
          @click="
            () => {
              $refs.flickity.stopPlayer()
              $refs.flickity.previous()
            }
          "
        >
          <!--prettier-ignore-->
          <svg width="50" height="50" viewBox="0 0 50 50" fill="none" xmlns="http://www.w3.org/2000/svg">
            <circle cx="25" cy="25" r="24.5" stroke="black"/>
            <path d="M34 25H16M16 25L23 18M16 25L23 32" stroke="black" stroke-opacity="0.95" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </button>
        <button
          @click="
            () => {
              $refs.flickity.stopPlayer()
              $refs.flickity.next()
            }
          "
        >
          <!--prettier-ignore-->
          <svg width="50" height="50" viewBox="0 0 50 50" fill="none" xmlns="http://www.w3.org/2000/svg">
            <circle cx="25" cy="25" r="24.5" transform="rotate(180 25 25)" stroke="black"/>
            <path d="M16 25H34M34 25L27 32M34 25L27 18" stroke="black" stroke-opacity="0.95" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </button>
      </div>
    </div>
    <client-only>
      <flickity
        ref="flickity"
        class="home__projects"
        :options="flickityOptions"
      >
        <a
          href="https://www.vistanium.com/"
          target="_blank"
          class="home__project home__project--vistanium"
        >
          <img
            src="@/assets/images/vistanium-mag-img.jpg"
            alt="Vistanium mag image"
          />
          <p class="u-font-normal">Vistanium Mag</p>
          <p>
            Immersive essays that narrate extraordinary true stories. They
            provide compelling insights into life in various cities, offering
            readers a rich, multifaceted perspective.
          </p>
        </a>
        <a
          href="https://podcasts.apple.com/us/podcast/i-too-sabi/id1653930660"
          target="_blank"
          class="home__project"
        >
          <img src="@/assets/images/i-too-sabi.jpg" alt="I too sabi image" />
          <p class="u-font-normal">I too sabi</p>
          <p>
            A Nigeria-focused conversational "ask me anything" podcast that
            answers a wide range of questions through research and expert
            insights.
          </p>
        </a>
        <a
          href="https://www.sunandcountry.com/"
          target="_blank"
          class="home__project home__project--sun-country"
        >
          <img
            src="@/assets/images/sun-and-country.svg"
            alt="Sun and Country image"
          />
          <p class="u-font-normal">Sun and Country</p>
          <p>
            A story-led guide to understanding the Nigerian Civil War, capturing
            the events that led to it, how it played out on all sides, and how
            it continues to shape our world today.
          </p>
        </a>
        <a
          href="https://podcasts.apple.com/za/podcast/i-like-girls/id1572625602/"
          target="_blank"
          class="home__project home__project--i-like-girls"
        >
          <img
            src="@/assets/images/i-like-girls.png"
            alt="I like girls image"
          />
          <p class="u-font-normal">I like girls</p>
          <p>
            A documentary-style, narrative-driven podcast exploring the diverse
            stories of African women. It offers firsthand insights into how
            gender shapes women's lives.
          </p>
        </a>
        <a
          href="https://hundredgood.com/"
          target="_blank"
          class="home__project"
        >
          <img
            src="@/assets/images/hundred-good.png"
            alt="Sun and Country image"
          />
          <p class="u-font-normal">HundredGood</p>
          <p>
            An annual curation of 100 good things that have happened across
            Africa. Every December, it offers a hopeful outlook on a continent
            riddled with a singular narrative of negativity.
          </p>
        </a>
      </flickity>
    </client-only>
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
  &__header {
    display: flex;
    justify-content: space-between;
    align-items: center;

    &-nav {
      button {
        background: transparent;
        border: none;

        &:not(:last-child) {
          margin-right: 1.3rem;
        }
      }

      @include screen(small) {
        display: none;
      }
    }
  }

  &__projects {
    position: relative;
    width: 100vw;
    left: calc(-50vw + 50%);
    margin-top: 5.2rem;

    @include screen(med) {
      margin-top: 4rem;
    }
  }

  &__project {
    --size: 25vw;
    width: var(--size);
    margin-right: 5rem;
    text-decoration: none;
    color: unset;

    @include screen(med) {
      --size: 40vw;
      margin-right: 4rem;
    }

    @include screen(small) {
      --size: 70vw;
      margin-right: 3rem;
    }

    img {
      width: var(--size);
      height: var(--size);
      background: rgb(220, 220, 220);
      object-fit: cover;
      border: 1px solid #000000;
      border-radius: 100px;
    }

    .u-font-normal {
      margin: 3rem 0 1rem;
    }

    &--sun-country {
      img {
        padding: 6rem 4.8rem;
        border-radius: 100%;
        background: white;
      }
    }

    &--vistanium img {
      border-radius: 30px;
    }
  }

  &__collaborations {
    margin-top: 26rem;

    @include screen(med) {
      margin-top: 18rem;
    }

    @include screen(small) {
      margin-top: 12rem;
    }

    &-subtext {
      max-width: 90rem;
      text-align: center;
      margin: 0 auto;

      @include screen(med) {
        text-align: left;
      }
    }

    &-brands {
      display: flex;
      margin: 7rem auto 0;
      width: fit-content;

      @include screen(med) {
        flex-wrap: wrap;
        width: auto;

        img {
          margin-bottom: 2.4rem;
        }
      }

      img:not(:last-child) {
        transform: scale(0.9);
        margin-right: 3rem;

        @include screen(small) {
          transform: scale(0.8);
          margin-right: 0rem;
        }
      }
    }
  }
}
</style>

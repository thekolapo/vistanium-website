<template>
  <div class="team">
    <div class="team__heading">
      <h1 class="u-font-h1">THE VISTANIUM</h1>
      <h1 class="u-font-h1">TEAM.</h1>
    </div>
    <div class="team__members">
      <div class="team__member">
        <p>
          Fuad Lawal is a seasoned media and tech operator with a decade-long
          experience in shaping businesses at various levels. Most recently, he
          served as the Editor in Chief at Big Cabal Media and led the growth
          and marketing team at Eden Life.
        </p>
        <img src="@/assets/images/fuad.jpg" alt="Fuad's picture" />
      </div>
      <div class="team__member">
        <p>
          Nana-Aisha Salaudeen is an award-winning storyteller with experience
          in producing content across diverse formats, including audio, text,
          and videos. She most recently worked as a multi-platform producer at
          CNN, covering a variety of business, tech, culture, and art stories
          across over 20 African countries.
        </p>
        <img src="@/assets/images/aisha.jpg" alt="Aisha's picture" />
      </div>
      <div class="team__member">
        <p>
          Ted Oladele was Vice President of Design & product development at
          Flutterwave where he led a talented team that specialized in Product
          Design, User Research, Brand, and Marketing Design.
        </p>
        <img src="@/assets/images/ted.jpg" alt="Ted's picture" />
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
.team {
  &__members {
    margin-top: 5.2rem;
    display: flex;
    flex-wrap: wrap;
  }

  &__member {
    width: 33%;

    img {
      width: 100%;
      margin-top: 7rem;
      border-radius: 20px;
      height: 44rem;
      object-fit: cover;
      object-position: top;
      align-self: flex-end;
      justify-self: flex-end;

      @include screen(med) {
        margin-top: 2rem;
        height: auto;
        max-height: 70rem;
      }

      @include screen(small) {
        max-height: 36rem;
      }
    }

    &:nth-child(1) {
      padding-right: 2.4rem;

      img {
        align-self: flex-end;
        justify-self: flex-end;
        margin-bottom: 0;
      }
    }

    &:nth-child(2) {
      border-left: 1px solid black;
      border-right: 1px solid black;
      padding: 0 2.4rem;
    }

    &:nth-child(3) {
      padding-left: 2.4rem;
    }

    @include screen(med) {
      width: 100%;

      &:not(:last-child) {
        margin-bottom: 6rem;
      }

      &:nth-child(1),
      &:nth-child(2),
      &:nth-child(3) {
        padding: 0;
        border: none;
      }
    }
  }
}
</style>

<template>
  <footer class="footer">
    <p class="footer__partnership-text">
      For collaboration or partnership discussions, please reach out via email
      to
      <a href="mailto:hello@vistanium.com" target="_blank">
        hello@vistanium.com
      </a>
    </p>
    <div class="footer__bottom">
      <div class="footer__copyright">
        <img src="@/assets/images/vistanium.svg" alt="vistanium logo" />
        <p>Vistanium {{ new Date().getFullYear() }}</p>
      </div>
      <div class="footer__social-links">
        <a href="https://www.youtube.com/@Vistanium" target="_blank">Youtube</a>
        <a href="https://www.instagram.com/vistanium" target="_blank">
          Instagram
        </a>
        <a href="https://twitter.com/Vistanium" target="_blank">Twitter</a>
      </div>
      <div class="footer__subscribe">
        <p>Stay up to date with our projects and stories</p>
        <form
          id="mc-embedded-subscribe-form"
          action="https://gmail.us14.list-manage.com/subscribe/post?u=c5e7be0fab293c70ce7928551&amp;id=5fb28450d7&amp;f_id=006188e0f0"
          method="post"
          name="mc-embedded-subscribe-form"
          validate
          class="footer__subscribe-form"
        >
          <input
            id="mce-EMAIL"
            name="EMAIL"
            type="email"
            required
            placeholder="Enter your email"
          />
          <button type="submit">Subscribe</button>
        </form>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
.footer {
  margin-top: 24rem;
  font-size: 2rem;

  @include screen(med) {
    margin-top: 16rem;
  }

  @include screen(small) {
    margin-top: 11rem;
  }

  a {
    color: black;
  }

  &__partnership-text {
    font-size: 3.6rem;
    line-height: 4rem;
    max-width: 144rem;

    @include screen(med) {
      font-size: 3rem;
      line-height: 3.4rem;
    }

    @include screen(small) {
      font-size: 2.6rem;
      line-height: 3.2rem;
    }
  }

  &__bottom {
    position: relative;
    margin-top: 4.6rem;
    padding-top: 4rem;
    display: flex;
    align-items: center;

    @include screen(small) {
      flex-wrap: wrap;
    }

    &::before {
      content: '';
      position: absolute;
      width: 100vw;
      top: 0;
      border-top: 1px solid #000000;
      height: 1px;
      left: calc(-50vw + 50%);
    }
  }

  &__copyright {
    width: 50%;
    margin-right: 5rem;

    img {
      margin-bottom: 2rem;
    }
  }

  &__social-links {
    display: flex;
    flex-direction: column;
    margin-right: 5rem;

    @include screen(small) {
      margin-right: 0;
      margin-left: auto;
    }

    a:not(:last-child) {
      margin-bottom: 1rem;
    }
  }

  &__subscribe {
    margin-left: auto;
    width: 100%;
    max-width: 54rem;

    @include screen(small) {
      max-width: unset;
      width: 100%;
      margin-top: 4rem;
    }

    &-form {
      border: 1px solid #1e1e1e;
      border-radius: 10px;
      padding: 1.6rem 2rem;
      background: white;
      margin-top: 1rem;
      display: flex;

      @include screen(small) {
        padding: 1.4rem 0.8rem;
      }

      input,
      button {
        border: none;
        background: transparent;
      }

      input {
        width: 100%;
        font-size: 1.8rem;
      }

      button {
        text-transform: uppercase;
        color: black;
        margin-left: 1rem;
      }
    }
  }
}
</style>

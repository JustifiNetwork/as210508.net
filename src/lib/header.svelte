<script lang="ts">
  let navOpen = false
</script>

<input type="checkbox" class="toggle-nav" aria-label="Toggle navigation" />

<aside>
  <a href="/"><img src="/logo.svg" alt="AS210508" /></a>
  <p>AS210508<br /><small>Justifi Network</small></p>

  <nav>
    <a href="#Home">Home</a>
    <a href="#Peering">Peering</a>
    <a href="#Abuse">Abuse</a>
    <a href="#Contact">Contact</a>
    <a target="_blank" href="https://status.as210508.net">Status</a>
    <a target="_blank" href="https://justifinetwork.com">Justifi Network</a>
  </nav>

  <div class="socials">
    <a target="_blank" href="https://github.com/JustifiNetwork">
      <img src="/social/github.svg" alt="github" />
    </a>
    <a target="_blank" href="https://twitter.com/JustifiNetwork">
      <img src="/social/twitter.svg" alt="twitter" />
    </a>
    <a target="_blank" href="https://www.linkedin.com/company/JustifiNetwork">
      <img src="/social/linkedin.svg" alt="linkedin" />
    </a>
  </div>
</aside>

<style lang="scss">
  aside {
    background: var(--almost-black);
    padding: 5rem;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    color: var(--winter-morning);

    height: 100vh;
    width: 100%;

    overflow-y: auto;

    position: fixed;
    top: 0;
    left: -100%;
    z-index: 10;

    transition: left 500ms ease;

    img {
      height: 7.5rem;
      margin-bottom: 0;
    }

    p {
      text-align: center;
      font-weight: bold;
      font-size: 1.25rem;
      line-height: 105%;
      margin-top: 1rem;

      small {
        opacity: 0.75;
        font-size: 0.75rem;
      }
    }

    nav {
      display: flex;
      flex-direction: column;
      justify-content: flex-start;
      align-items: center;
      margin-top: 2rem;

      * + * {
        margin-top: 1rem;
      }

      a {
        color: var(--winter-morning);
        opacity: 0.75;
        text-decoration: none;
        font-size: 1.125rem;
        transition: opacity 200ms ease;

        &:hover {
          opacity: 1;
        }
      }
    }

    .socials {
      margin-top: 2rem;

      * + * {
        margin-left: 1rem;
      }

      img {
        height: 1.5rem;
        filter: invert(1);
        opacity: 0.75;
        transition: opacity 300ms ease;

        &:hover {
          opacity: 1;
        }
      }
    }
  }

  [type='checkbox'] {
    all: unset;
    z-index: 100;
    font-size: 2rem;

    &,
    &::before,
    &::after {
      position: fixed;
      top: 2rem;
      right: 2rem;
    }

    &::before,
    &::after {
      font-family: FontAwesome;
      font-weight: normal;
      font-style: normal;
      text-decoration: none;
      transition: transform 300ms ease, opacity 300ms ease, filter 300ms ease;
    }

    &::before {
      content: '\f00d';
      right: 2.3rem;
      opacity: 0;
      transform: rotate(-180deg);
    }

    &::after {
      content: '\f0c9';
      right: 2.1rem;
      opacity: 1;
      transform: rotate(0deg);
    }

    &:checked {
      background: blue;

      & + aside {
        left: 0;
      }

      &::before {
        transform: rotate(0deg);
        opacity: 1;
        filter: invert(1);
      }

      &::after {
        transform: rotate(180deg);
        opacity: 0;
      }
    }
  }

  @media screen and (min-width: 600px) {
    aside {
      position: sticky;
      top: 0;
      left: 0;
      width: auto;
    }

    .toggle-nav {
      display: none;
    }
  }
</style>

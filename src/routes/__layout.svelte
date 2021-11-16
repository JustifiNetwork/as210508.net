<script lang="ts">
  import '../global.scss'
</script>

<main>
  <aside>
    <a href="/" class="logo-anchor">
      <img src="/justifi.svg" alt="" />
      <p>as210508</p>
    </a>
    <p><small>Justifi Network</small></p>

    <nav>
      <a href="/">Home</a>
    </nav>
  </aside>

  <slot />
</main>

<style lang="scss">
  main {
    display: grid;
    grid-template-columns: 1fr 5fr;
    font-family: var(--font-sans);
  }

  aside {
    position: sticky;
    top: 0;
    bottom: 0;

    background: var(--clr-almost-black);
    color: var(--clr-winter-morning);
    display: flex;
    justify-content: flex-start;
    align-items: center;
    flex-direction: column;
    padding: 5rem 2rem;

    .logo-anchor {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      color: var(--clr-winter-morning);
      text-decoration: none;

      p {
        margin-top: 1rem;
        text-transform: uppercase;
        font-size: 1.4rem;
        font-weight: 700;
      }
    }

    nav {
      margin-top: 1rem;

      a {
        color: var(--clr-mountain-side);
        text-decoration: none;
        font-size: 1.2rem;
        transition: color var(--transition);

        &:hover {
          color: var(--clr-cold-winds);
        }
      }
    }

    small {
      font-size: 1rem;
      color: var(--clr-mountain-side);
    }
  }
</style>

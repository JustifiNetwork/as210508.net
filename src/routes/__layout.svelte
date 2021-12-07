<script lang="ts">
  import '../global.scss'
  import Header from '$lib/header.svelte'
</script>

<Header />

<main>
  <slot />
</main>

<style lang="scss">
  main {
    padding: 5rem 0;
    margin: 0 auto;

    width: min(80ch, 80%);
  }

  @media screen and (min-width: 600px) {
    :global(body) {
      display: grid;
      grid-template-areas: '. .';
      grid-template-columns: 1fr 5fr;
    }
  }
</style>

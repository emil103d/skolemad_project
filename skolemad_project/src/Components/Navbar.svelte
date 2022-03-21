<script>
  import Hamburger from "svelte-hamburgers";
  let open;
</script>

<Hamburger bind:open />

{#if open}
  <div>
    <a href="#/forside" on:click={() => (page = "forside")}>Forside</a>
    <a href="#/bestil_mad" on:click={() => (page = "bestilmad")}>Bestil Mad</a>
    <a href="#/minkonto" on:click={() => (page = "minkonto")}>Min Konto</a>
    <a href="#/tankop" on:click={() => (page = "tankop")}>Tank op</a>
  </div>
{/if}

<style>
  div {
    display: flex;
    flex-direction: column;
    gap: 4rem;
    padding: 5rem 4rem;
    position: absolute;
    background-color: var(--bgcolor);
    width: 100vw;
    font-size: var(--font_b);
  }

  @media (min-width: 810px) {
  }
</style>

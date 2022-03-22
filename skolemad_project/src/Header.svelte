<script>
  import Hamburger from "svelte-hamburgers";
  import Navbar from "./Navbar.svelte";
  let open;
</script>

<div class="hamburger"><Hamburger bind:open --color="black" /></div>

{#if open}
  <div><Navbar bind:open /></div>
{/if}

<style>
  div {
    margin-bottom: 2rem;
  }

  @media (min-width: 800px) {
    .hamburger {
      display: none;
    }
  }
</style>

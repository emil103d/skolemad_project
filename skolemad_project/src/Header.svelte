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

  /* .bignav {
    display: none;
  } */

  @media (min-width: 800px) {
    .hamburger,
    .navbar {
      display: none;
    }

    .bignav {
      display: block;
    }
  }
</style>

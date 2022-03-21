<script>
  import Hamburger from "svelte-hamburgers";
  import Navbar from "./Navbar.svelte";
  let open;
</script>

<Hamburger bind:open --color="black" />

{#if open}
  <div><Navbar bind:open /></div>
{/if}

<style>
  div {
    margin-bottom: 2rem;
  }
</style>

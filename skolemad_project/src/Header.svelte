<script>
  import Hamburger from "svelte-hamburgers";
  import Navbar from "./Navbar.svelte";
  import BigNav from "./Navbarbig.svelte";
  import NavBarLogin from "./NavbarLogin.svelte";
  let open;
</script>

<div class="hamburger"><Hamburger bind:open --color="black" /></div>

{#if open}
  <div><Navbar bind:open /></div>
{/if}

<BigNav />

<style>
  .bignav {
    display: none;
  }
  div {
    margin-bottom: 2rem;
  }

  @media (min-width: 800px) {
    .hamburger,
    .navbar {
      display: none;
    }
  }

  @media (min-width: 800px) {
    .bignav {
      display: block;
    }
  }
</style>

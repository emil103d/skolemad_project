<script>
  import Header from "./Header.svelte";
  import Footer from "./Components/Footer.svelte";
  import Hamburger from "svelte-hamburgers";
  import Navbar from "./Navbar.svelte";
  let open;
</script>

<body>
  <Header />

  <Hamburger bind:open --color="black" />

  {#if open}
    <Navbar />
  {/if}

  <!-- <Navbar>
    <a href="#/forside" on:click={() => (page = "forside")}>Forside</a>
    <a href="#/bestil_mad" on:click={() => (page = "bestilmad")}>Bestil Mad</a>
    <a href="#/minkonto" on:click={() => (page = "minkonto")}>Min Konto</a>
    <a href="#/tankop" on:click={() => (page = "tankop")}>Tank op</a>
  </Navbar>
  {#if page === "forside"}
    <Forside />
  {:else if page === "bestilmad"}
    <Bestil_mad />
  {:else if page === "minkonto"}
    <Min_konto />
  {:else if page === "tankop"}
    <Tank_op />
  {/if} -->
  <main />
  <Footer />
</body>

<style>
</style>

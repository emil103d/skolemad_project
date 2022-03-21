<script>
  import Header from "./Header.svelte";
  import Navbar from "./Components/Navbar.svelte";
  import Forside from "./Components/Navbar.svelte";
  import Bestil_mad from "./Bestil_mad.svelte";
  import Min_konto from "./Min_konto.svelte";
  import Tank_op from "./Tank_op.svelte";
  import Footer from "./Components/Footer.svelte";
  let page = "forside";
</script>

<body>
  <Header />
  <Navbar>
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
  {/if}
  <main />
  <Footer />
</body>

<style>
</style>

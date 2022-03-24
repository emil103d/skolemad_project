<script>
  import Header from "./Header.svelte";
  import Footer from "./Components/Footer.svelte";
  import Forside from "./Forside.svelte";
  import Bestil_mad from "./Bestil_mad.svelte";
  import Min_konto from "./Min_konto.svelte";
  import Tank_op from "./Tank_op.svelte";
  import Hamburger from "svelte-hamburgers";
  import Navbar from "./Navbar.svelte";
  import BigNav from "./Navbarbig.svelte";
  import NavBarLogin from "./NavbarLogin.svelte";
  let page = "forside";
  let open;
</script>

<body>
  <div class="hamburger"><Hamburger bind:open --color="black" /></div>

  {#if open}
    <div><Navbar bind:open /></div>
  {/if}
  {#if page === "forside"}
    <Forside />
  {:else if page === "bestilmad"}
    <Bestil_mad />
  {:else if page === "minkonto"}
    <Min_konto />
  {:else if page === "tankop"}
    <Tank_op />
  {/if}
  <Footer />
</body>

<style>
</style>

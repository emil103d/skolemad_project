<script>
  import { fly, scale } from "svelte/transition";
  import { quadOut } from "svelte/easing";
  import Forside from "./Forside.svelte";
  import Bestil_mad from "./Bestil_mad.svelte";
  import Min_konto from "./Min_konto.svelte";
  import Tank_op from "./Tank_op.svelte";
  let page = "forside";
  export let open;
</script>

{#if open}
  <div class="navbar">
    <a
      transition:fly={{ y: -15, delay: 50 }}
      href="#/forside"
      on:click={() => (page = "forside")}>Forside</a
    >
    <a
      transition:fly={{ y: -15, delay: 70 }}
      href="#/bestil_mad"
      on:click={() => (page = "bestilmad")}>Bestil Mad</a
    >
    <a
      transition:fly={{ y: -15, delay: 60 }}
      href="#/minkonto"
      on:click={() => (page = "minkonto")}>Min Konto</a
    >

    <a
      transition:fly={{ y: -15, delay: 50 }}
      href="#/tankop"
      on:click={() => (page = "tankop")}>Tank op</a
    >
  </div>
  <hr transition:scale={{ duration: 750, easing: quadOut, opacity: 1 }} />
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

<div class="bignav">
  <div class="toppart">
    <p>Opret Bruger</p>
    <p>Log ind</p>
  </div>

  <div class="lowerpart">
    <img src="" alt="" />
    <div>
      <p>Forældre</p>
      <p>Skole</p>
      <p>Leverandør</p>
    </div>
  </div>
</div>

<style>
  .navbar {
    font-size: var(--font_b);
    padding: 7rem 0;
    padding-top: 0;
    font-weight: 200;
  }
  a {
    cursor: pointer;
    display: block;
    width: max-content;
    margin: 1rem auto;
  }

  .toppart {
    background-color: var(--primary);
    color: white;
    font-size: var(--font_bl);
    text-decoration: underline;
  }

  .lowerpart {
    display: flex;
    flex-direction: row;
  }

  .hamburger {
  }
</style>

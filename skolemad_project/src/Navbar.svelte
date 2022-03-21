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

<div .navbar>
  <div>
    <div transition:fly={{ y: -15, delay: 50 * i }}><a href="#/forside" on:click={() => (page = "forside")}>Forside</a></div>
    <div transition:fly={{ y: -15, delay: 50 * i }}>
      <a href="#/bestil_mad" on:click={() => (page = "bestilmad")}>Bestil Mad</a
      >
      </div>
    <p transition:fly={ y: -15, delay: 50 * i }> 
      <a href="#/minkonto" on:click={() => (page = "minkonto")}>Min Konto</a>
    </p>
    <p transition:fly={ y: -15, delay: 50 * i }><a href="#/tankop" on:click={() => (page = "tankop")}>Tank op</a></p>
  </div>
  {#if page === "forside"}
    <Forside />
  {:else if page === "bestilmad"}
    <Bestil_mad />
  {:else if page === "minkonto"}
    <Min_konto />
  {:else if page === "tankop"}
    <Tank_op />
  {/if}
      <hr transition:scale={{ duration: 750, easing: quadOut, opacity: 1 }} />
</navbar>

<style>

  .navbar {
    text-align: center;
    font-size: 1.5em;
    letter-spacing: 0.15em;
    padding: 1em;
    padding-top: 0;
    color: #eef;
  }
  div {
    cursor: pointer;
    width: max-content;
    margin: 1rem auto;
  }
  p:hover {
    text-decoration: underline;
  }
</style>

<script>
  export let type;
</script>

<button class={type}> <slot /> </button>

<!-- 
    button:hover {
    filter: brightness(1.5);
  }

  .primary {
    background-color: var(--blue);
  }

  .secondary {
    background-color: var(--pink);
  }  -->
<style>
  button {
    background-color: var(--primary);
    border-radius: var(--border-radius-md);
    color: var(--hvid);
    font-size: var(--font_knap);
  }
</style>

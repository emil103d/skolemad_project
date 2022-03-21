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
  .primary {
    background-color: var(--primary);
    border-radius: var(--border-radius-md);
    color: var(--hvid);
    font-size: var(--font_knap);
    padding: 10px 45px;
    border-style: none;
  }
  .secondary {
    background-color: var(--secondary);
    border-radius: var(--border-radius-sm);
    color: var(--primary);
    font-size: var(--font_knap);
    padding: 5px 20px;
    border-style: none;
  }

  button:hover {
    opacity: 75%;
  }
</style>

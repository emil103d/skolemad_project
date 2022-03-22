<script>
  import Content from "./Content.svelte";
  import Modal from "./Modal.svelte";
  import Pop_up from "./Pop_up.svelte";
  import { modal } from "./stores.js";
</script>

<Modal show={$modal}>
  <Content />
</Modal>

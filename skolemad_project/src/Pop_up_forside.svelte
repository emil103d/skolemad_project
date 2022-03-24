<script>
	import Modal,{getModal} from './Modal_forside.svelte'
  import Bestil_mad from "./Bestil_mad.svelte";
  import goto  from './Bestil_mad.svelte';

	let selection
  let page = "bestilmad";
	
	// Callback function provided to the `open` function, it receives the value given to the `close` function call, or `undefined` if the Modal was closed with escape or clicking the X, etc.
	function setSelection(res){
		selection=res
	}
	
</script>

<!-- Simplest use: modal without an `id` or callback function -->
<button on:click={()=>getModal().open()}>
	Opret ny bruger
</button>

<!-- the modal without an `id` -->
<Modal>
	<h1>Opret bruger</h1>

  <form action="log-ind">
    <input
      type="text"
      placeholder="Fornavn"
      id="fornavn"
      name="fornavn"
    /><br /> <br />
    <input
      type="text"
      id="efternavn"
      placeholder="Efternavn"
      name="efternavn"
    /><br /><br />
    <input
    type="text"
    id="Telefonnummer"
    placeholder="Telefonnummer"
    name="Telefonnummer"
    /><br /><br />
    <input
      type="text"
      placeholder="E-mail"
      id="e-mail"
      name="e-mail"
    /><br /> <br />
    <input
      type="text"
      id="password"
      placeholder="Password"
      name="password"
    /><br /><br />
    <input
      type="text"
      id="gpassword"
      placeholder="Gentag password"
      name="gpassword"
    /><br /><br />

  </form>




	<!-- opening a model with an `id` and specifying a callback	 -->
	<button on:click={() => (page = "Bestil_mad")}>
		Opret 
	</button>	
</Modal>




<style>
	/* The content inside the modal can be styled as usual	 */
	.green {
		background: #0f0;
	}

  h1 {
    padding-bottom: var(--spacing-20);
  }

  form {

  }
</style>
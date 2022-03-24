<script>
	import Modal,{getModal} from './Modal_forside.svelte'
	let name = 'world';
	
	let selection
	
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
      placeholder="E-mail"
      id="e-mail"
      name="e-mail"
    /><br /> <br />
    <input
      type="text"
      id="Telefonnummer"
      placeholder="Telefonnummer"
      name="Telefonnummer"
    /><br /><br />




  </form>




	<!-- opening a model with an `id` and specifying a callback	 -->
	<button on:click={()=>getModal('second').open(setSelection)}>
		Open Nested Popup
	</button>
	{#if selection}
	<p>
		Your selection was: {selection}
	</p>
	{/if}
</Modal>

<Modal id="second">
	Inner window
	<!-- Passing a value back to the callback function	 -->
	<button class="green" on:click={()=>getModal('second').close(1)}>
		Select 1
	</button>
	<button class="green" on:click={()=>getModal('second').close(2)}>
		Select 2
	</button>
	
</Modal>

<style>
	/* The content inside the modal can be styled as usual	 */
	.green {
		background: #0f0;
	}
</style>
<script>
  import Modal, { getModal } from "./Modal.svelte";
  import PrimaryButton from "./Components/Primary_button.svelte";
  export let month;
  export let pris;
  export let total_pris;
  export let child1;
  export let child2;

  let selection;

  // Callback function provided to the `open` function, it receives the value given to the `close` function call, or `undefined` if the Modal was closed with escape or clicking the X, etc.
  function setSelection(res) {
    selection = res;
  }
</script>

<!-- Simplest use: modal without an `id` or callback function -->
<button on:click={() => getModal().open()}> Bestil mad </button>

<!-- the modal without an `id` -->
<Modal>
  <article class="container">
    <div class="title">
      <h3>BESTIL: {month}</h3>
      <p>Din saldo:{pris} kr.</p>
    </div>
    <div class="mini_container">
      <h4>1. VÆLG</h4>
      <div class="barn">
        <p>{child1}</p>
        <label class="switch">
          <input type="checkbox" />
          <span class="slider round" />
        </label>
      </div>
      <div class="barn">
        <p>{child2}</p>
        <label class="switch">
          <input type="checkbox" />
          <span class="slider round" />
        </label>
      </div>
      <div class="mini_container">
        <h4>2. Pris</h4>
        <p>Total {total_pris}</p>
      </div>
      <div class="mini_container">
        <h4>3. Betaling</h4>
        <div class="knapper">
          <div class="knap">
            <PrimaryButton type="primary">Mobilepay</PrimaryButton>
          </div>
          <div class="knap">
            <PrimaryButton type="primary">Kontobetaling</PrimaryButton>
          </div>
          <p>Tank Konto op</p>
        </div>
      </div>
    </div>
  </article>

  <!-- opening a model with an `id` and specifying a callback	 -->
  <button on:click={() => getModal("second").open(setSelection)}>
    Betal og bekræft
  </button>
</Modal>

<Modal id="second">
  <h2>Tak for din bestilling</h2>

  <p>Din konto er nu 0kr.</p>

  <svg
    width="135"
    height="168"
    viewBox="0 0 135 168"
    fill="none"
    xmlns="http://www.w3.org/2000/svg"
  >
    <path
      d="M68.1438 53.2488C79.387 48.7663 91.9217 48.8822 103.081 53.572C114.241 58.2618 123.145 67.1554 127.899 78.3606C135.317 94.8597 131.007 110.284 127.899 121.379C124.551 133.559 118.208 144.69 109.457 153.742C101.062 162.218 94.8901 163.883 92.3972 164.337C86.8945 165.626 81.1223 165.024 75.998 162.627C72.8321 161.071 70.0395 158.839 67.8134 156.088C66.3125 158.124 64.461 159.873 62.3471 161.249C51.4143 168.212 36.9975 161.915 34.6848 160.901C14.9368 152.258 8.82467 128.251 6.00137 117.202C3.67366 108.12 1.13566 97.5238 4.98015 84.8392C7.80299 75.9165 12.9968 67.9435 19.9977 61.7859C25.5047 56.547 32.2112 52.7616 39.5204 50.7664C49.0761 48.4423 59.1225 49.3136 68.1438 53.2488Z"
      fill="#82A875"
      stroke="white"
      stroke-width="5"
      stroke-miterlimit="10"
      stroke-linecap="round"
    />
    <path
      d="M83.1764 6.09768C79.5221 14.0192 75.8779 21.9307 72.2437 29.8321C71.1761 24.2532 68.7101 19.0423 65.0803 14.6953C52.2704 -0.320313 30.3448 3.29742 28.7529 3.58502C28.7529 5.09869 29.0983 20.9317 42.539 30.5284C54.8834 39.338 68.3842 35.8414 70.2013 35.3419C69.8859 37.5216 69.6156 39.8072 69.3753 42.1685C69.125 44.8225 68.9448 47.3453 68.8347 49.7369"
      fill="#82A875"
    />
    <path
      d="M83.1764 6.09768C79.5221 14.0192 75.8779 21.9307 72.2437 29.8321C71.1761 24.2532 68.7101 19.0423 65.0803 14.6953C52.2704 -0.320313 30.3448 3.29742 28.7529 3.58502C28.7529 5.09869 29.0983 20.9317 42.539 30.5284C54.8834 39.338 68.3842 35.8414 70.2013 35.3419C69.8859 37.5216 69.6156 39.8072 69.3753 42.1685C69.125 44.8225 68.9448 47.3453 68.8347 49.7369"
      stroke="white"
      stroke-width="5"
      stroke-miterlimit="10"
      stroke-linecap="round"
    />
    <path
      d="M17.8953 86.7012C14.7694 100.763 17.1414 115.498 24.5181 127.843"
      stroke="white"
      stroke-width="3"
      stroke-miterlimit="10"
      stroke-linecap="round"
    />
    <path
      d="M36.291 144.418C34.7443 144.086 33.341 143.27 32.2814 142.087C31.0938 140.762 30.2525 139.159 29.8335 137.425"
      stroke="white"
      stroke-width="3"
      stroke-miterlimit="10"
      stroke-linecap="round"
    />
  </svg>

  <!-- Passing a value back to the callback function	 -->
  <button on:click={() => getModal("second").close(1)}> Log ud </button>
  <button on:click={() => getModal("second").close(2)}> Tank op </button>
</Modal>

<style>
  .container {
    background: var(--primary);
    border-radius: var(--border-radius-sm);
    width: auto;
    margin: auto;
    padding-bottom: 1rem;
  }

  h3,
  h4,
  p {
    text-align: center;
    padding: 0.2rem;
  }

  .mini_container {
    background: white;
    margin: 1rem;
    padding: 1rem;
    border-radius: 1rem;
  }
  .barn {
    display: flex;
    align-items: center;
    gap: 1rem;
    justify-content: center;
    margin: 0.2rem;
  }

  .knap {
    margin-top: 1rem;
    display: flex;
    justify-content: center;
  }

  button {
    margin: auto;
    margin-top: 1rem;
    display: flex;
    justify-content: center;
  }

  .knapper {
    display: block;
    justify-content: center;
    gap: 1rem;
  }

  .title h3 {
    color: white;
  }

  .title p {
    color: white;
  }

  /* The switch - the box around the slider */
  .switch {
    position: relative;
    display: inline-block;
    width: 60px;
    height: 34px;
  }

  /* Hide default HTML checkbox */
  .switch input {
    opacity: 0;
    width: 0;
    height: 0;
  }

  /* The slider */
  .slider {
    position: absolute;
    cursor: pointer;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: #ccc;
    -webkit-transition: 0.4s;
    transition: 0.4s;
  }

  .slider:before {
    position: absolute;
    content: "";
    height: 26px;
    width: 26px;
    left: 4px;
    bottom: 4px;
    background-color: white;
    -webkit-transition: 0.4s;
    transition: 0.4s;
  }

  input:checked + .slider {
    background-color: var(--primary);
  }

  input:focus + .slider {
    box-shadow: 0 0 1px #2196f3;
  }

  input:checked + .slider:before {
    -webkit-transform: translateX(26px);
    -ms-transform: translateX(26px);
    transform: translateX(26px);
  }

  /* Rounded sliders */
  .slider.round {
    border-radius: 34px;
  }

  .slider.round:before {
    border-radius: 50%;
  }

  @media (min-width: 800px) {
    .container {
      padding: 2rem;
    }

    .knapper {
      display: flex;
      justify-content: center;
      gap: 1rem;
    }
  }
</style>

<script>
  import PrimaryButton from "./Components/Primary_button.svelte";
</script>

<article class="container">
  <h2>Heeeeej</h2>
</article>

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

  .knapper {
    display: block;
    justify-content: center;
    gap: 1rem;
  }

  .main_knap {
    display: flex;
    justify-content: center;
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

<script>
  import Uge_menu from "./Components/Uge_menu.svelte";
</script>

<main>
  <img src="img/madder.png" alt="" />
  <h2>Månedens mad</h2>
  <div class="frokost_menuer">
    <div class="underoverskrift">
      <svg
        width="19"
        height="25"
        viewBox="0 0 19 25"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path d="M18 24L1 12.5L18 1" stroke="black" />
      </svg>
      <h3>Frokoster for februar</h3>
      <svg
        width="19"
        height="25"
        viewBox="0 0 19 25"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path d="M1 1L18 12.5L1 24" stroke="black" />
      </svg>
    </div>
    <div class="menuer">
      <Uge_menu
        uge="5"
        dato="9. feb - 12.feb"
        tema_categori="Jorden Rundt"
        man_ret="Pitabrød m. Kebab"
        tirs_ret="Sweet potato suppe"
        ons_ret="Gryderet med kartofler i karry sauce"
        tors_ret="Club Sandwich"
        fre_ret="Pasta med Kødsovs"
      />
    </div>
  </div>
</main>

<style>
  .frokost_menuer {
    background-color: beige;
  }
  img {
    width: 100%;
    height: 16rem;
    object-fit: cover;
  }

  .underoverskrift {
    display: flex;
    align-items: center;
    gap: 2rem;
    justify-content: center;
    background: var(--lightgrey);
  }

  h3 {
    margin: 0;
  }
</style>

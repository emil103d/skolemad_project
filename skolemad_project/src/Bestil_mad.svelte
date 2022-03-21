<script>
  import Uge_menu from "./Components/Uge_menu.svelte";
  import Primary_button from "./Components/Primary_button.svelte";
  import PrimaryButton from "./Components/Primary_button.svelte";
</script>

<main>
  <img src="img/madder.png" alt="" />
  <section class="first_section">
    <h2>Månedens mad</h2>
    <div class="frokost_menuer">
      <div class="underoverskrift">
        <svg
          width="16"
          height="25"
          viewBox="0 0 19 25"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path d="M18 24L1 12.5L18 1" stroke="black" />
        </svg>
        <h3>Frokoster for februar</h3>
        <svg
          width="16"
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
          tema_categori="Verdenen"
          man_ret="Pitabrød m. Kebab"
          tirs_ret="Sweet potato suppe"
          ons_ret="Gryderet med kartofler i karry sauce"
          tors_ret="Club Sandwich"
          fre_ret="Pasta med Kødsovs"
        />

        <Uge_menu
          uge="6"
          dato="9. feb - 12.feb"
          tema_categori="Natur"
          man_ret="Pitabrød m. Kebab"
          tirs_ret="Sweet potato suppe"
          ons_ret="Gryderet med kartofler i karry sauce"
          tors_ret="Club Sandwich"
          fre_ret="Pasta med Kødsovs"
        />

        <Uge_menu
          uge="7"
          dato="9. feb - 12.feb"
          tema_categori="Efterår"
          man_ret="Pitabrød m. Kebab"
          tirs_ret="Sweet potato suppe"
          ons_ret="Gryderet med kartofler i karry sauce"
          tors_ret="Club Sandwich"
          fre_ret="Pasta med Kødsovs"
        />

        <Uge_menu
          uge="8"
          dato="9. feb - 12.feb"
          tema_categori="Mad modig"
          man_ret="Pitabrød m. Kebab"
          tirs_ret="Sweet potato suppe"
          ons_ret="Gryderet med kartofler i karry sauce"
          tors_ret="Club Sandwich"
          fre_ret="Pasta med Kødsovs"
        />
      </div>
      <PrimaryButton type="primary">Bestil her</PrimaryButton>
    </div>
  </section>
</main>

<style>
  .frokost_menuer {
    background-color: var(--grey);
    padding: 1rem;
  }

  .menuer {
    display: flex;
    gap: 1rem;
    justify-content: center;
    margin: 1rem;
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
    margin: 1rem;
  }

  h3 {
    margin: 0;
  }
</style>

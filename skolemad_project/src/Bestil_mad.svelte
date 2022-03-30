<script>
  import Uge_menu from "./Components/Uge_menu.svelte";
  import PrimaryButton from "./Components/Primary_button.svelte";
  import Oversigt_md_bestil from "./Components/Oversigt_md_bestil.svelte";
  import Pop_up_bestil from "./Pop_up_bestil.svelte";
</script>

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

    <div class="button">
      <Pop_up_bestil
        month="FEBRUAR"
        pris="350"
        total_pris="500kr"
        child1="Frida"
        child2="Carlo"
      />
      <!-- 
      <div id="state">
        {#if opening}
          <p>opening modal...</p>
        {:else if opened}
          <p>opened modal!</p>
        {:else if closing}
          <p>closing modal...</p>
        {:else if closed}
          <p>closed modal!</p>
        {/if} -->
      <!-- </div> -->
    </div>
  </div>
</section>

<section>
  <h2>Oversigt over bestillinger</h2>
  <div class="oversigt">
    <Oversigt_md_bestil month="Januar" child1="Frida" child2="Carlo" />
    <Oversigt_md_bestil month="Februar" child1="Frida" child2="Carlo" />
    <Oversigt_md_bestil month="Marts" child1="Frida" child2="Carlo" />
    <Oversigt_md_bestil month="April" child1="Frida" child2="Carlo" />
    <Oversigt_md_bestil month="Maj" child1="Frida" child2="Carlo" />
    <Oversigt_md_bestil month="Juni" child1="Frida" child2="Carlo" />
    <Oversigt_md_bestil month="Juli" child1="Frida" child2="Carlo" />
    <Oversigt_md_bestil month="August" child1="Frida" child2="Carlo" />
    <Oversigt_md_bestil month="September" child1="Frida" child2="Carlo" />
    <Oversigt_md_bestil month="Oktober" child1="Frida" child2="Carlo" />
    <Oversigt_md_bestil month="November" child1="Frida" child2="Carlo" />
    <Oversigt_md_bestil month="December" child1="Frida" child2="Carlo" />
  </div>
</section>

<style>
  #state {
    position: absolute;
    top: 0;
    right: 0;
    opacity: 0.33;
    font-size: 0.8em;
  }
  .frokost_menuer {
    background-color: var(--grey);
    padding: 1rem;
    justify-content: center;
  }

  .menuer {
    display: grid;
    grid-template-columns: repeat(1, 14rem);
    gap: 1rem;
    justify-content: center;
    margin: 1rem;
  }
  img {
    width: 100%;
    height: 16rem;
    object-fit: cover;
  }

  .button {
    display: flex;
    justify-content: center;
    margin: auto;
  }

  .underoverskrift {
    display: flex;
    align-items: center;
    gap: 2rem;
    justify-content: center;
    background: var(--lightgrey);
    margin: 1rem;
  }

  /* h2 {
    margin: 1rem;
    margin-top: 4rem;
    margin-bottom: 2rem;
  }

  h3 {
    margin: 0;
  } */

  section {
    padding: var(--spacing-20);
  }

  h2 {
    padding-bottom: var(--spacing-20);
  }
  .oversigt {
    display: grid;
    grid-template-columns: repeat(1, 14rem);
    gap: 1rem;
    justify-content: center;
    margin-left: 5rem;
    margin-right: 5rem;
    margin-bottom: 5rem;
  }

  @media (min-width: 400px) {
    .menuer {
      display: grid;
      grid-template-columns: repeat(2, 14rem);
    }

    .oversigt {
      display: grid;
      grid-template-columns: repeat(2, 14rem);
    }
  }

  @media (min-width: 600px) {
    .menuer {
      display: grid;
      grid-template-columns: repeat(2, 17rem);
    }
  }

  @media (min-width: 800px) {
    .oversigt {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
    }
  }

  @media (min-width: 950px) {
    .menuer {
      display: flex;
      gap: 1rem;
      justify-content: center;
      margin: 1rem;
    }
    .oversigt {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
    }
  }
</style>

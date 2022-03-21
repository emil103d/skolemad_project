<script>
  export let uge;
  export let dato;
  export let tema_categori;
  export let man_ret;
  export let tirs_ret;
  export let ons_ret;
  export let tors_ret;
  export let fre_ret;
</script>

<article class="container">
  <div class="title">
    <h3>Uge{uge}</h3>
    <p>{dato}</p>
  </div>
  <img src="img/ret1.png" alt="" />
  <div>
    <h4>Tema: {tema_categori}</h4>
    <p>Manadag: {man_ret}</p>
    <p>Tirsdag: {tirs_ret}</p>
    <p>Onsdag: {ons_ret}</p>
    <p>Torsdag: {tors_ret}</p>
    <p>Fredag: {fre_ret}</p>
  </div>
</article>

<style>
  .container {
    background: white;
    border-radius: var(--border-radius-sm);
    min-width: 14rem;
    max-width: 17rem;
    padding-top: 1rem;
  }

  .title {
    text-align: center;
  }

  div {
    margin: 1rem;
  }

  .title p {
    margin-bottom: 1rem;
  }

  h4 {
    margin-block: 1rem;
  }

  img {
    width: 100%;
    object-fit: cover;
  }
</style>

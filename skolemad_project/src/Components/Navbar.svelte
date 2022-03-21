<script>
window.addEventListener("load", sidenVises);

function sidenVises() {
    const burgerKnap = document.querySelector("#burger_knap");
    burgerKnap.addEventListener("click", toggleMenu);

} 

function toggleMenu() {
    const burgerKnap = this;
    const menu = document.querySelector("#menu");

    burgerKnap.classList.toggle("open");
    menu.classList.toggle("open");
}
</script>


<header>
  <nav>
      <div class="logo">
        <a href="index.html">
          <p><u> A</u>MADEUS NOAH JENSEN</p>
        </a>
    </div>

      <ul id="menu">
        <li><a href="index.html" id="forside">FORSIDE</a></li>
        <li><a href="about.html" id="about">ABOUT</a></li>
        <li><a href="projects.html" id="projects">PROJECTS</a></li>
        <li><a href="contact.html" id="contact">CONTACT</a></li>
      </ul>

      <div id="burger_knap">
        <div class="streg top"></div>
        <div class="streg center"></div>
        <div class="streg bottom"></div>
      </div>
    </nav>
</header>



<nav>
  <slot />
</nav>

<style>
  header {
    position: sticky;
    left: 0;
    top: 0;
    height: 70px;
    width: 100%;
    padding-top: 20px;
    background-color: white;
}

header nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

#menu {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    background-color: white;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding-bottom: 10px;
    justify-content: center;
    gap: 15px;
    transition: transform 0.3s;
    transform: translateX(-100%);
}

#menu.open {
    transform: translateX(0);
}

#menu a {
    display: block;
    text-align: center;
    color: black;
}

#menu a:hover {
    color: #192F37
}

#burger_knap {
    width: 30px;
    height: 30px;
    background-color: transparent;
    overflow: hidden;
    position: relative;
}

.streg {
    width: 100%;
    height: 2px;
    position: absolute;
    background-color: black;
    top: calc(50%);
    left: 0;
    transition: transform 0.3s, opacity 0.3s;
}

.streg.top {
    transform: translateY(-10px);
}

.streg.bottom {
    transform: translateY(10px);
}


/* #burger_knap */
#burger_knap.open .streg.top {
    transform: translateY(0) rotate(45deg);
}

#burger_knap.open .streg.center {
    transform: translateX(100%);
    opacity: 0;
}

#burger_knap.open .streg.bottom {
    transform: translateY(0) rotate(-45deg);
}
</style>

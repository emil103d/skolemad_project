<script>

</script>

<body>
    <main>
        <!-- Section 1 -->
        <section class="section_1_forside">
            <article class="section_1_container">
                <h1>Velkommen til skolemad</h1>
                <p>SkoleMad tilbyder et system til at styre fleksibel og rationel levering af skolemad, mad til firmaer, mad ud af huset, take-away, pensionistmad og meget mere. </p>
                <div class="log_ind">
                    <h3>Log ind</h3>
                    <form action="/action_page.php">
                        <input type="text" placeholder="Brugernavn" id="username" name="username"><br> <br>
                        <input type="text" id="lname" placeholder="password" name="password"><br><br>
                      </form>
                    <div class="login_bar">
                        <button>Log ind</button>
                        <a href="">Opret ny bruger</a>
                    </div>
                </div>
            </article>
        </section>


        <!-- Section 2 -->
        <section class="section_2_forside">

        </section>
    </main>
</body>


<style>
    
    section {
        padding: var(--spacing-20);
    }

    .section_1_forside {
        background-image: url(/img/madder.png);
        background-size: cover;
        background-position: 40%;
        height: 100vh;
        width: 100vw;
        display: grid;
        align-items: center;
    }
    

    .section_1_container {
        background-color: var(--hvid);
        border-radius: var(--border-radius-sm);
        padding: var(--spacing-20);
        display: grid;
        gap: var(--spacing-20)
    }

    h1{
        font-size: var(--font_xl);
    }

    h3 {
        color: var(--hvid);
    }

    .log_ind {
        background: var(--primary);
        border-radius: var(--border-radius-sm);
        padding: var(--spacing-15);
        padding-top: var(--spacing-30);
        padding-bottom: var(--spacing-30);
    }

    button {
        background-color: var(--secondary);
        border-radius: var(--border-radius-sm);
    }

    input {
        width: 100%;
    }

    a {
        color: var(--hvid);
    }

    .login_bar {
        display: flex;
        justify-content: space-between;
    }
    

</style>
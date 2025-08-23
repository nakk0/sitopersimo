<script>
    import foto1 from "$lib/images/foto1.png";
    import foto2 from "$lib/images/foto2.png";
    import foto3 from "$lib/images/foto3.png";
    let isMenuOpen = false;

    function toggleMenu() {
        isMenuOpen = !isMenuOpen;
    }
</script>

<style>
    body {
        font-family: 'Arial', sans-serif;
        margin: 0;
        padding: 0;
        background-color: #f4f4f4;
    }

    .navbar {
        background-color: #333;
        color: white;
        padding: 10px 20px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        position: relative;
    }

    .navbar a {
        color: white;
        text-decoration: none;
        padding: 10px;
    }

    .navbar .menu {
        display: flex;
        gap: 15px;
    }

    .hamburger {
        display: none;
        cursor: pointer;
        font-size: 24px;
    }

    .navbar a:hover {
        background-color: #ddd;
        color: black;
    }

    .container {
        display: flex;
        flex-wrap: wrap;
        padding: 20px;
        gap: 20px;
    }

    .main-content {
        flex: 1 1 600px;
        padding: 20px;
        background-color: white;
        border-radius: 5px;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }

    .article-title {
        color: #333;
        font-size: 28px;
        font-weight: bold;
        margin-bottom: 20px;
    }

    .article-content {
        font-size: 18px;
        line-height: 1.6;
        color: #555;
        margin-bottom: 20px;
    }

    .highlight {
        color: #d9534f;
        font-weight: bold;
    }

    .sidebar {
        flex: 0 1 250px;
        padding: 20px;
        background-color: #e9ecef;
        border-radius: 5px;
    }

    .sidebar h3 {
        font-size: 22px;
        color: #333;
        margin-bottom: 15px;
    }

    .sidebar ul {
        list-style-type: none;
        padding: 0;
    }

    .sidebar ul li {
        margin-bottom: 10px;
    }

    .sidebar ul li a {
        text-decoration: none;
        color: #d9534f;
    }

    .sidebar ul li a:hover {
        text-decoration: underline;
    }

    .footer {
        background-color: #333;
        color: white;
        text-align: center;
        padding: 10px 0;
        margin-top: 20px;
    }

    /* Media Queries per il layout responsivo */
    @media (max-width: 768px) {
        .navbar {
            flex-wrap: wrap;
            padding: 10px;
        }

        .navbar .menu {
            display: none;
            flex-direction: column;
            width: 100%;
            background-color: #333;
            position: absolute;
            top: 50px;
            left: 0;
            transition: all 0.3s ease;
        }

        .navbar .menu.open {
            display: flex;
        }

        .navbar .menu a {
            padding: 15px;
            border-bottom: 1px solid #444;
            text-align: left;
        }

        .hamburger {
            display: block;
        }
    }
</style>

<!-- Contenuto HTML -->
<div class="navbar">
    <div class="hamburger" on:click={toggleMenu}>&#9776;</div>
    <div class={`menu ${isMenuOpen ? 'open' : ''}`}>
        <a href="#home">Home</a>
        <a href="#cultura">Cultura</a>
        <a href="#musica">Musica</a>
        <a href="#eventi">Eventi</a>
        <a href="#contatti">Contatti</a>
    </div>
</div>

<div class="container">
    <!-- Main Content -->
    <div class="main-content">
        <h1 class="article-title">Cala del Rosso, occhi puntati sull'orizzonte: attesa un'onda anomala nelle prossime ore</h1>
        <img src={foto1} alt="Foto cala rosso" style="width: 100%;">
        <p class="article-content">
            <span class='highlight'>Fertilia (SS)</span> — Le condizioni del mare davanti alla Cala del Rosso stanno cambiando in modo insolito. Diversi indicatori tecnici raccolti oggi descrivono un possibile innalzamento improvviso del moto ondoso su un fronte stretto, con formazione di un'onda isolata in grado di superare nettamente l'altezza media delle onde attuali. L'evento, se confermato, potrebbe presentarsi senza un segnale evidente fino a pochi istanti prima dell'impatto a riva.
        </p>
        <img src={foto2} alt="altra foto cala rosso" style="width: 100%;">
        <p class='article-content'>Secondo le analisi preliminari, nelle prossime ore potrebbero verificarsi:</p>
        <ul>
            <li><p class='article-content'><b>pause anomale tra un'onda e l'altra</b>, con lunghi secondi di calma apparente</p></li>
            <li><p class='article-content'><b>una linea scura e netta all'orizzonte</b> che avanza più veloce del normale</p></li>
            <li><p class='article-content'><span class="highlight">un ritiro dell'acqua insolitamente marcato subito prima dell'arrivo del fronte</span></p></li>
        </ul>
        <p class="article-content">
            I modelli indicano che il punto più esposto sarebbe il <span class="highlight">piccolo anfiteatro di roccia a sinistra della cala</span> guardando il mare, dove i riflessi del fondale creano correnti laterali che possono incanalare l'energia dell'onda. Il fenomeno potrebbe manifestarsi in un'unica cresta rilevante oppure in due impulsi ravvicinati, con la seconda onda più irregolare della prima.
        </p>
        <img src={foto3} alt="altra foto cala rosso" style="width: 100%;">
        <p class="article-content">
            Le autorità non parlano più solo di prudenza: <span class="highlight">è stato emesso un ordine di evacuazione immediata dell'area della Cala del Rosso.</span> Tutti i presenti sono invitati a lasciare la spiaggia e le scogliere senza indugi, portando con sé solo l'essenziale.
            È stato inoltre richiesto ai diportisti di <span class="highlight">mollare subito gli ormeggi e allontanarsi con le barche dalla linea costiera</span>, perché l'onda potrebbe spingere con violenza i natanti contro gli scogli e le banchine.
            Chi si attarda rischia di trovarsi intrappolato dal fronte d'acqua che potrebbe abbattersi senza preavviso.
        </p>
        
    </div>

    <!-- Sidebar -->
    <div class="sidebar">
        <h3>Altri Articoli</h3>
        <ul>
            <li><a href="#notizia1">Il ritorno dei vinili: perché i giovani amano la musica retrò</a></li>
            <li><a href="#notizia2">Concerti estivi: le tappe da non perdere questa estate</a></li>
            <li><a href="#notizia3">Intervista esclusiva a Gianna Nannini: "La mia musica, la mia vita"</a></li>
            <li><a href="#notizia4">Nuovi talenti della scena indie: chi sono e dove ascoltarli</a></li>
            <li><a href="#notizia5">Le 10 canzoni italiane che hanno fatto la storia del pop</a></li>
        </ul>
    </div>
</div>

<div class="footer">
    © 2025 La Gazzetta di Fertilia - Tutti i diritti riservati
</div>
    
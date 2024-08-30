<script>
    import foto1 from "$lib/images/foto1.jpg";
    import foto2 from "$lib/images/foto2.jpg";
    import foto3 from "$lib/images/foto3.jpg";
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
        <h1 class="article-title">Il Bar Biancone Rinnova il Piano Bar: Dal Punk Rock al Pop</h1>
        <img src={foto1} alt="Foto del Bar Biancone" style="width: 100%;">
        <p class="article-content">
            <span class="highlight">Il Biancone cambia veste</span>: storico locale noto per i concerti di <span class="highlight">punk rock</span> e <span class="highlight">blues</span>, il <em>Bar Biancone</em> ha deciso di sorprendere ancora una volta il suo affezionato pubblico con una trasformazione radicale. Dai <span class="highlight">Metallica</span> a <span class="highlight">Lucio Battisti</span>, la rivoluzione è servita.
        </p>
        <p class="article-content">
            Conosciuto per anni come uno dei pochi luoghi in cui respirare l'atmosfera del vero rock underground, il <em>Bar Biancone</em> era sinonimo di serate energiche, piene di chitarre elettriche distorte e batterie incalzanti. Ma oggi, il locale ha deciso di puntare su un'esperienza completamente diversa: <span class="highlight">piano bar</span> e musica pop. "I ragazzi del Biancone si sono inteneriti," scherza uno dei clienti abituali. 
        </p>
        <img src={foto2} alt="Altra Foto del Bar Biancone" style="width: 100%;">
        <p class="article-content">
            "Sono passati dal pogare ai tavolini con le tovaglie a quadretti," commenta un altro frequentatore ridendo. "Probabilmente tra poco inizieranno anche a servire tisane rilassanti al posto della birra!" L’ironia è palpabile, ma molti riconoscono che il nuovo format ha un suo fascino particolare.
        </p>
        <p class="article-content">
            Le nuove serate al Biancone sembrano uscite da un vecchio film romantico, con luci soffuse, candele e una playlist che spazia da Elton John a qualche sconosciuto crooner locale. "Ormai manca solo che si metta qualcuno a leggere poesie," commenta sarcastico un giovane cliente. "A questo punto possiamo aspettarci anche una degustazione di formaggi francesi!"
        </p>
        <img src={foto3} alt="Altra Foto del Bar Biancone" style="width: 100%;">
        <p class="article-content">
            Nonostante il cambiamento radicale, il <em>Bar Biancone</em> non dimentica le sue radici. Ogni venerdì sera sarà ancora dedicato a serate a tema rock e punk, con l'obiettivo di mantenere viva l'anima che ha reso famoso il locale. Ma i fan del vecchio Biancone sono ancora perplessi: "Chissà, magari tra un po' vedremo anche i DJ set di baby dance," conclude scherzosamente un avventore.
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
    © 2024 La Gazzetta del Giorno - Tutti i diritti riservati
</div>

<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Página oficial de Milenium Tvi: transmisiones en vivo, noticias, videos y entretenimiento en Ecuador.">
    <meta name="keywords" content="noticias Ecuador, TV en vivo, Milenium Tvi, Daniel Noboa, entrevistas, series, películas">
    <meta property="og:title" content="Milenium Tvi: Noticias, Transmisiones en Vivo y Entretenimiento en Ecuador">
    <meta property="og:description" content="Tu fuente de entretenimiento, noticias y mucho más en Milenium Tvi.">
    <meta property="og:image" content="https://mileniumtvi.com/logo.png">
    <meta property="og:url" content="https://mileniumtvi.com">
    <meta property="og:type" content="website">
    <title>Milenium Tvi - Inicio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css">
    <!-- Video.js CSS -->
    <link href="https://vjs.zencdn.net/8.10.0/video-js.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }
        body {
            background-color: #4682B4;
            color: #333;
        }
        /* Header */
        header {
            background: linear-gradient(90deg, #1a73e8, #0d47a1);
            color: white;
            padding: 1rem 2rem;
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        .header-container {
            max-width: 1400px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .logo img {
            height: 50px;
        }
        nav {
            display: flex;
            justify-content: center;
            align-items: center;
            width: 100%;
        }
        nav ul {
            list-style: none;
            display: flex;
            gap: 0.8rem;
            align-items: center;
            flex-wrap: wrap;
            justify-content: center;
        }
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s;
            font-size: 0.95rem;
            padding: 0.5rem;
        }
        nav ul li a:hover,
        nav ul li a:focus {
            color: #ffd700;
            outline: 2px solid #ffd700;
        }
        .menu-toggle {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: white;
        }
        /* Hero Section */
        .hero {
            background: url('https://mileniumtvi.com/banner-hero.jpg') no-repeat center/cover;
            height: 500px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
        }
        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }
        .hero button {
            background: #ffd700;
            border: none;
            padding: 0.75rem 1.5rem;
            font-size: 1.1rem;
            cursor: pointer;
            border-radius: 5px;
            transition: background 0.3s;
        }
        .hero button:hover {
            background: #e6c200;
        }
        /* Sections */
        .section {
            padding: 2rem 1rem;
            max-width: 1400px;
            margin: 0 auto;
        }
        .section h2 {
            font-size: 1.8rem;
            margin-bottom: 1.2rem;
            color: #ffd700;
        }
        #live h2 {
            color: #1a73e8;
        }
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 1rem;
        }
        .card {
            background: white;
            border-radius: 10d;
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }
        .card:hover {
            transform: translateY(-5px);
        }
        .card img {
            width: 100%;
            height: 140px;
            object-fit: cover;
        }
        .card-content {
            padding: 0.8rem;
        }
        .card-content h3 {
            font-size: 1.1rem;
            margin-bottom: 0.4rem;
        }
        .card-content p {
            font-size: 0.85rem;
            color: #666;
        }
        /* Live Stream Section */
        .live-stream {
            background: #f9f9f9;
            text-align: center;
        }
        .live-stream .video-js {
            width: 100%;
            max-width: 800px;
            height: 450px;
            margin: 1rem auto;
        }
        /* Entrevistas Section */
        .entrevistas-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 1rem;
        }
        .entrevistas-container .video-wrapper {
            position: relative;
            width: 100%;
            max-width: 800px;
            padding-bottom: 56.25%;
            height: 0;
            overflow: hidden;
        }
        .entrevistas-container .video-wrapper iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        }
        .entrevistas-container p {
            font-size: 0.95rem;
            color: #333;
            max-width: 800px;
            text-align: center;
        }
        /* Footer */
        footer {
            background: #0d47a1;
            color: white;
            padding: 1.5rem;
            text-align: center;
        }
        footer a {
            color: #ffd700;
            text-decoration: none;
        }
        footer a:hover {
            text-decoration: underline;
        }
        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 1.8rem;
            }
            .menu-toggle {
                display: block;
            }
            nav ul {
                display: none;
                flex-direction: column;
                position: absolute;
                top: 100%;
                left: 0;
                right: 0;
                background: #0d47a1;
                padding: 1rem;
                text-align: center;
            }
            nav ul.active {
                display: flex;
            }
            nav ul li {
                margin: 0.5rem 0;
            }
            nav ul li a {
                font-size: 1rem;
                padding: 0.5rem;
            }
            .live-stream .video-js {
                height: 200px;
            }
            .entrevistas-container .video-wrapper {
                max-width: 100%;
                padding-bottom: 56.25%;
            }
            .entrevistas-container p {
                font-size: 0.85rem;
                padding: 0 0.8rem;
            }
            .section {
                padding: 1.5rem 0.8rem;
            }
            .section h2 {
                font-size: 1.5rem;
            }
            .card img {
                height: 120px;
            }
            .card-content h3 {
                font-size: 1rem;
            }
            .card-content p {
                font-size: 0.8rem;
            }
        }
        @media (max-width: 480px) {
            .hero h1 {
                font-size: 1.5rem;
            }
            .hero button {
                font-size: 1rem;
                padding: 0.6rem 1.2rem;
            }
            .grid {
                grid-template-columns: 1fr;
            }
        }

        /* CARRUSEL DE PRUEBA - ESTILOS */
        .carousel-container {
            position: relative;
            overflow: hidden;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            background: #fff;
        }
        .carousel-track {
            display: flex;
            transition: transform 0.5s ease;
            gap: 20px;
            padding: 20px 0;
        }
        .carousel-card {
            min-width: 300px;
            max-width: 300px;
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            position: relative;
        }
        .carousel-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.2);
        }
        .carousel-card img {
            width: 100%;
            height: 180px;
            object-fit: cover;
            transition: transform 0.4s ease;
        }
        .carousel-card:hover img {
            transform: scale(1.08);
        }
        .carousel-content {
            padding: 16px;
        }
        .carousel-content h3 {
            margin: 0 0 8px 0;
            font-size: 1.1rem;
            color: #1a1a1a;
            line-height: 1.3;
            display: -webkit-box;
            -webkit-line-clamp: 2;
            -webkit-box-orient: vertical;
            overflow: hidden;
        }
        .carousel-content p {
            margin: 0;
            font-size: 0.85rem;
            color: #555;
            display: -webkit-box;
            -webkit-line-clamp: 3;
            -webkit-box-orient: vertical;
            overflow: hidden;
        }
        .carousel-content a {
            display: inline-block;
            margin-top: 10px;
            color: #0066cc;
            font-weight: 600;
            font-size: 0.85rem;
            text-decoration: none;
        }
        .carousel-content a:hover {
            text-decoration: underline;
        }
        .carousel-btn {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            background: rgba(0,0,0,0.5);
            color: white;
            border: none;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            font-size: 1.5rem;
            cursor: pointer;
            z-index: 10;
        }
        .carousel-btn.prev { left: 15px; }
        .carousel-btn.next { right: 15px; }

        @media (max-width: 768px) {
            .carousel-card { min-width: 260px; max-width: 260px; }
            .carousel-btn { width: 40px; height: 40px; font-size: 1.2rem; }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="header-container">
            <div class="logo">
                <img src="https://mileniumtvi.com/logo.png" alt="Logo de Milenium Tvi">
            </div>
            <i class="fas fa-bars menu-toggle" aria-label="Abrir menú"></i>
            <nav>
                <ul>
                    <li><a href="#live" aria-label="Ir a Transmisiones en Vivo">Transmisiones en Vivo</a></li>
                    <li><a href="#tvplay" aria-label="Ir a TV Play">TV Play</a></li>
                    <li><a href="#news" aria-label="Ir a Noticias">Noticias</a></li>
                    <li><a href="#videos" aria-label="Ir a Videos">Videos</a></li>
                    <li><a href="#posts" aria-label="Ir a Publicaciones">Publicaciones</a></li>
                    <li><a href="#imagenes" aria-label="Ir a Noticia en Imágenes">Noticia en Imágenes</a></li>
                    <li><a href="#defensa" aria-label="Ir a Defensa del Televidente">Defensa del Televidente</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div>
            <h1>Bienvenidos a Milenium Tvi</h1>
            <p>Tu fuente de entretenimiento, noticias y mucho más</p>
            <button onclick="window.location.href='#live'" aria-label="Ver transmisión en vivo ahora">Ver Ahora</button>
        </div>
    </section>

    <!-- Transmisiones en Vivo -->
    <section id="live" class="section live-stream">
        <h2>Transmisiones en Vivo</h2>
        <div class="entrevistas-container">
            <div class="video-wrapper">
                <iframe src="https://app.viloud.tv/embed/channel/c8984eee3163b175a0c725860f53749d?autoplay=false&muted=false" width="100%" height="360" frameborder="0" allowfullscreen allow="autoplay; encrypted-media" title="Transmisión en vivo del canal principal de Milenium Tvi"></iframe>
            </div>
            <p>Transmisión en vivo del canal principal de Milenium Tvi.</p>

            <div class="video-wrapper">
                <iframe src="https://app.viloud.tv/embed/channel/119c56a41cef4bf9b47e6d600cc70a63?autoplay=false&muted=false" width="100%" height="360" frameborder="0" allowfullscreen allow="autoplay; encrypted-media" title="MTVI2 Musical - Música en vivo"></iframe>
            </div>
            <p>Disfruta de la mejor selección de música en vivo con MTVI2 Musical.</p>

            <div class="video-wrapper">
                <iframe src="https://app.viloud.tv/embed/channel/fa28724c715bb373296ca57a2dcd551c?autoplay=false&muted=false" width="100%" height="360" frameborder="0" allowfullscreen allow="autoplay; encrypted-media" title="MTVI3 Películas - Streaming continuo"></iframe>
            </div>
            <p>Las mejores películas en streaming continuo con MTVI3 Películas.</p>

            <div class="video-wrapper">
                <iframe src="https://app.viloud.tv/embed/channel/8823313f19b20ef55dea4f3ad8a4cab7?autoplay=false&muted=false" width="100%" height="360" frameborder="0" allowfullscreen allow="autoplay; encrypted-media" title="MTVI4 Series - Tus series favoritas en vivo"></iframe>
            </div>
            <p>Tus series favoritas en transmisión en vivo con MTVI4 Series.</p>
        </div>
    </section>

    <!-- TV Play -->
    <section id="tvplay" class="section">
        <h2>TV Play</h2>
        <div class="grid">
            <div class="card">
                <iframe loading="lazy" width="100%" height="315" src="https://www.youtube.com/embed/brgDCi26lUQ?si=Hhr-ETQKVjf_nl5S" title="Expresión Popular con Diego Idrovo" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                <div class="card-content">
                    <h3>Expresión Popular con Diego Idrovo</h3>
                    <p>Diego Idrovo, Presidente de la Cámara de Transporte de Cuenca, analiza la tarifa del servicio urbano de buses en #ExpresionPopular</p>
                </div>
            </div>
            <!-- ... (otros videos de TV Play) ... -->
        </div>
    </section>

    <!-- Noticias -->
    <section id="news" class="section">
        <h2>Noticias</h2>
        <div class="grid">
            <!-- ... (noticias existentes) ... -->
        </div>
    </section>

    <!-- Noticias Locales -->
    <section id="locales" class="section">
        <h2>Noticias Locales</h2>
        <div class="grid">
            <!-- ... (noticias locales actualizadas) ... -->
        </div>
    </section>

    <!-- CARRUSEL DE PRUEBA -->
    <section id="carrusel-prueba" class="section" style="background: #f8f9fa; padding: 60px 0;">
        <div class="container" style="max-width: 1200px; margin: 0 auto; padding: 0 20px;">
            <h2 style="text-align: center; margin-bottom: 40px; color: #1a1a1a; font-size: 2rem;">Carrusel de Prueba - Vista Previa Automática</h2>
            
            <div class="carousel-container">
                <div class="carousel-track" id="carousel-track"></div>
                <button class="carousel-btn prev" onclick="moveCarousel(-1)">◄</button>
                <button class="carousel-btn next" onclick="moveCarousel(1)">►</button>
            </div>

            <p style="text-align: center; margin-top: 20px; color: #666; font-size: 0.9rem;">
                Imágenes y datos extraídos automáticamente vía Open Graph
            </p>
        </div>
    </section>

    <!-- Noticia en Imágenes -->
    <section id="imagenes" class="section">
        <h2>Noticia en Imágenes</h2>
        <div class="grid">
            <!-- ... (imágenes existentes) ... -->
        </div>
    </section>

    <!-- Videos -->
    <section id="videos" class="section">
        <h2>Videos</h2>
        <div class="grid">
            <!-- ... -->
        </div>
    </section>

    <!-- Publicaciones -->
    <section id="posts" class="section">
        <h2>Publicaciones</h2>
        <div class="grid">
            <!-- ... -->
        </div>
    </section>

    <!-- Defensa del Televidente -->
    <section id="defensa" class="section">
        <h2>Defensa del Televidente</h2>
        <p>En nuestro canal, tu voz importa. Contáctanos para cualquier queja, sugerencia o consulta.</p>
        <form action="/enviar-contacto" method="post">
            <label for="nombre">Nombre:</label>
            <input type="text" id="nombre" placeholder="Nombre" required>
            <label for="email">Correo Electrónico:</label>
            <input type="email" id="email" placeholder="Correo Electrónico" required>
            <label for="mensaje">Tu mensaje:</label>
            <textarea id="mensaje" placeholder="Tu mensaje" required></textarea>
            <button type="submit">Enviar</button>
        </form>
    </section>

    <!-- Footer -->
    <footer>
        <p>© <span id="current-year"></span> Milenium Tvi. Todos los derechos reservados.</p>
        <p><a href="/terminos" aria-label="Términos y Condiciones">Términos y Condiciones</a> | <a href="/privacidad" aria-label="Política de Privacidad">Política de Privacidad</a> | <a href="#defensa" aria-label="Contacto para Defensa del Televidente">Contacto</a></p>
        <div class="social">
            <a href="https://www.facebook.com/mileniumtvi/" target="_blank" rel="noopener noreferrer" aria-label="Facebook de Milenium Tvi"><i class="fab fa-facebook-f"></i></a>
            <a href="https://x.com/mileniumtvi" target="_blank" rel="noopener noreferrer" aria-label="X (Twitter) de Milenium Tvi"><i class="fab fa-x-twitter"></i></a>
            <a href="https://www.instagram.com/mileniumtvi/" target="_blank" rel="noopener noreferrer" aria-label="Instagram de Milenium Tvi"><i class="fab fa-instagram"></i></a>
            <a href="https://www.youtube.com/@mileniumtvi" target="_blank" rel="noopener noreferrer" aria-label="YouTube de Milenium Tvi"><i class="fab fa-youtube"></i></a>
        </div>
    </footer>

    <!-- Video.js Script -->
    <script src="https://vjs.zencdn.net/8.10.0/video.min.js"></script>
    <script>
        // Smooth scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({ behavior: 'smooth' });
            });
        });

        // Año dinámico
        document.getElementById('current-year').textContent = new Date().getFullYear();

        // Menú hamburguesa
        document.querySelector('.menu-toggle').addEventListener('click', () => {
            document.querySelector('nav ul').classList.toggle('active');
        });

        // CARRUSEL DE PRUEBA - SCRIPT
        const articles = [
            "https://mileniumtvi.com/gracias-por-no-olvidarse-de-nosotros-migrantes-en-estados-unidos-expresan-su-apoyo-a-daniel-noboa",
            "https://mileniumtvi.com/alcalde-zamora-hace-llamado-para-hacer-de-cuenca-una-ciudad-m-s-humana1",
            "https://mileniumtvi.com/el-presidente-noboa-cumple-con-la-comunidad-educativa-de-santo-domingo-entreg-la-u-e-san-jacinto-del-b-a",
            "https://mileniumtvi.com/n-una-noche-llena-de-emoci-n-elegancia-y-orgullo-cuencano-fue-elegida-martina-guzm-n-vega-como-reina-de-cuenca-2025-2026"
        ];

        const track = document.getElementById('carousel-track');
        let currentIndex = 0;

        articles.forEach(url => {
            fetch(`https://api.allorigins.win/get?url=${encodeURIComponent(url)}`)
                .then(response => response.json())
                .then(data => {
                    const parser = new DOMParser();
                    const doc = parser.parseFromString(data.contents, 'text/html');

                    const title = doc.querySelector('meta[property="og:title"]')?.content || "Sin título";
                    const description = doc.querySelector('meta[property="og:description"]')?.content || "Sin descripción.";
                    const image = doc.querySelector('meta[property="og:image"]')?.content || "https://via.placeholder.com/300x180";

                    const card = document.createElement('div');
                    card.className = 'carousel-card';
                    card.innerHTML = `
                        <a href="${url}" target="_blank" rel="noopener noreferrer">
                            <img src="${image}" alt="${title}" loading="lazy" onerror="this.src='https://via.placeholder.com/300x180?text=Imagen+no+disponible';">
                        </a>
                        <div class="carousel-content">
                            <h3>${title}</h3>
                            <p>${description}</p>
                            <a href="${url}" target="_blank" rel="noopener noreferrer">Leer más →</a>
                        </div>
                    `;
                    track.appendChild(card);
                })
                .catch(err => console.error("Error:", err));
        });

        function moveCarousel(direction) {
            const cards = document.querySelectorAll('.carousel-card');
            if (cards.length === 0) return;
            const cardWidth = cards[0].offsetWidth + 20;
            currentIndex = (currentIndex + direction + cards.length) % cards.length;
            track.style.transform = `translateX(-${currentIndex * cardWidth}px)`;
        }

        setInterval(() => moveCarousel(1), 6000);
    </script>
</body>
</html>

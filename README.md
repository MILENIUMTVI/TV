<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Página oficial de Milenium Tvi, tu fuente de transmisiones en vivo, noticias, entrevistas y entretenimiento.">
    <!-- Open Graph Meta Tags -->
    <meta property="og:title" content="Milenium Tvi - Noticias y Entretenimiento">
    <meta property="og:description" content="Disfruta de transmisiones en vivo, noticias, entrevistas y más en Milenium Tvi.">
    <meta property="og:image" content="https://mileniumtvi.com/wp-content/uploads/2025/07/logo-mileniumtvi.jpg">
    <meta property="og:url" content="https://mileniumtvi.com">
    <meta property="og:type" content="website">
    <!-- Twitter Card Meta Tags -->
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:title" content="Milenium Tvi - Noticias y Entretenimiento">
    <meta name="twitter:description" content="Disfruta de transmisiones en vivo, noticias, entrevistas y más en Milenium Tvi.">
    <meta name="twitter:image" content="https://mileniumtvi.com/wp-content/uploads/2025/07/logo-mileniumtvi.jpg">
    <!-- Mobile Web App -->
    <meta name="apple-mobile-web-app-capable" content="yes">
    <title>Milenium Tvi - Inicio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css" integrity="sha512-z3gLpd7yknf1YoNbCzqRKc4qyor8gaKU1qmn+CShxbuBusANI9QpRohGBreCFkKxLhei6S9CQXFEbbKuqLg0DA==" crossorigin="anonymous" referrerpolicy="no-referrer">
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
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: #ffd700;
            text-transform: uppercase;
        }

        nav {
            display: flex;
            align-items: center;
        }

        nav ul {
            list-style: none;
            display: flex;
            gap: 1.5rem;
            align-items: center;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s;
            white-space: nowrap;
        }

        nav ul li a:hover {
            color: #ffeb3b;
        }

        .menu-toggle {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
            background: none;
            border: none;
            color: white;
        }

        /* Hero Section */
        .hero {
            background: url('https://mileniumtvi.com/wp-content/uploads/2025/07/hero-image.jpg') no-repeat center/cover;
            height: 500px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .hero button {
            background: #ffd700;
            border: none;
            padding: 0.75rem 1.5rem;
            font-size: 1.2rem;
            cursor: pointer;
            border-radius: 5px;
            transition: background 0.3s;
        }

        .hero button:hover {
            background: #e6c200;
        }

        /* Sections */
        .section {
            padding: 3rem 1rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section h2 {
            font-size: 2rem;
            margin-bottom: 1.5rem;
            color: #ffd700;
            text-align: center;
        }

        #live h2 {
            color: #1a73e8;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
        }

        .card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }

        .card:hover {
            transform: translateY(-5px);
        }

        .card img {
            width: 100%;
            height: 150px;
            object-fit: cover;
            loading: lazy;
        }

        .card-content {
            padding: 1rem;
        }

        .card-content h3 {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
        }

        .card-content p {
            font-size: 0.9rem;
            color: #666;
            margin-bottom: 0.5rem;
        }

        .card-content a {
            color: #1a73e8;
            text-decoration: none;
            font-weight: bold;
        }

        .card-content a:hover {
            text-decoration: underline;
        }

        /* Live Stream Section */
        .live-stream {
            background: #f9f9f9;
            text-align: center;
        }

        .live-stream .video-js {
            width: 100%;
            max-width: 800px;
            height: auto;
            aspect-ratio: 16/9;
            margin: 1rem auto;
        }

        /* Entrevistas Section */
        .entrevistas-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 1.5rem;
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
            loading: lazy;
        }

        .entrevistas-container p {
            font-size: 1rem;
            color: #333;
            max-width: 800px;
            text-align: center;
        }

        /* Formulario */
        .form-group {
            margin-bottom: 1rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: bold;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 0.5rem;
            border: 1px solid #ccc;
            border-radius: 5px;
            font-size: 1rem;
        }

        .form-group textarea {
            resize: vertical;
            min-height: 100px;
        }

        .form-group button {
            background: #1a73e8;
            color: white;
            border: none;
            padding: 0.75rem 1.5rem;
            cursor: pointer;
            border-radius: 5px;
            font-size: 1rem;
            transition: background 0.3s;
        }

        .form-group button:hover {
            background: #0d47a1;
        }

        .honeypot {
            display: none;
        }

        /* Footer */
        footer {
            background: #0d47a1;
            color: white;
            padding: 2rem 1rem;
            text-align: center;
        }

        footer a {
            color: #ffeb3b;
            text-decoration: none;
            margin: 0 0.5rem;
        }

        footer a:hover {
            text-decoration: underline;
        }

        .social {
            margin-top: 1rem;
        }

        .social a {
            margin: 0 0.5rem;
            font-size: 1.2rem;
        }

        /* Back to Top Button */
        .back-to-top {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: #1a73e8;
            color: white;
            border: none;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: none;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            font-size: 1.2rem;
            z-index: 1000;
            transition: background 0.3s;
        }

        .back-to-top:hover {
            background: #0d47a1;
        }

        .back-to-top.show {
            display: flex;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .hero {
                height: 300px;
            }

            .hero h1 {
                font-size: 2rem;
            }

            .hero p {
                font-size: 1rem;
            }

            .hero button {
                padding: 0.5rem 1rem;
                font-size: 1rem;
            }

            nav ul {
                display: none;
                flex-direction: column;
                gap: 1rem;
                position: absolute;
                top: 60px;
                left: 0;
                width: 100%;
                background: #0d47a1;
                padding: 1rem;
                text-align: center;
            }

            nav ul.show {
                display: flex;
            }

            .menu-toggle {
                display: block;
            }

            .live-stream .video-js {
                max-width: 100%;
                height: auto;
            }

            .entrevistas-container .video-wrapper {
                max-width: 100%;
            }

            .section {
                padding: 2rem 0.5rem;
            }

            .grid {
                grid-template-columns: 1fr;
            }

            .card iframe {
                height: 200px;
            }
        }

        @media (max-width: 480px) {
            .hero h1 {
                font-size: 1.5rem;
            }

            .section h2 {
                font-size: 1.5rem;
            }

            .card-content h3 {
                font-size: 1rem;
            }

            .card-content p {
                font-size: 0.85rem;
            }

            .form-group input,
            .form-group textarea {
                font-size: 0.9rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header role="banner">
        <div class="header-container">
            <div class="logo">Milenium Tvi</div>
            <nav aria-label="Navegación principal">
                <button class="menu-toggle" aria-label="Abrir menú de navegación" aria-expanded="false">
                    <i class="fas fa-bars"></i>
                </button>
                <ul>
                    <li><a href="#live">Transmisiones en Vivo</a></li>
                    <li><a href="#tvplay">TV Play</a></li>
                    <li><a href="#news">Noticias</a></li>
                    <li><a href="#videos">Videos</a></li>
                    <li><a href="#posts">Publicaciones</a></li>
                    <li><a href="#imagenes">Noticia en Imágenes</a></li>
                    <li><a href="#defensa">Defensa del Televidente</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" role="banner">
        <div>
            <h1>Bienvenidos a Milenium Tvi</h1>
            <p>Tu fuente de entretenimiento, noticias y mucho más</p>
            <button onclick="window.location.href='#live'">Ver Ahora</button>
        </div>
    </section>

    <!-- Main Content -->
    <main role="main">
        <!-- Transmisiones en Vivo -->
        <section id="live" class="section live-stream">
            <h2>Transmisiones en Vivo</h2>
            <video
                id="live-stream-player"
                class="video-js vjs-default-skin"
                controls
                preload="auto"
                data-setup='{}'>
                <source src="https://app.viloud.tv/hls/channel/c8984eee3163b175a0c725860f53749d.m3u8" type="application/x-mpegURL">
                <p class="vjs-no-js">
                    Para ver este video, habilita JavaScript y considera actualizar a un navegador que soporte video HTML5.
                </p>
            </video>
        </section>

        <!-- Entrevistas -->
        <section id="entrevistas" class="section live-stream">
            <h2>Entrevistas</h2>
            <div class="entrevistas-container">
                <div class="video-wrapper">
                    <iframe
                        src="https://www.youtube.com/embed/t6AcnjKj4xo"
                        title="Suspensión de operaciones de la Cooperativa CREA Ltda."
                        frameborder="0"
                        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                        allowfullscreen
                        loading="lazy">
                    </iframe>
                </div>
                <p>La SEPS dispone la suspensión de operaciones y liquidación forzosa de la Cooperativa CREA Ltda., garantizando la protección de los depósitos de los socios.</p>
                <div class="video-wrapper">
                    <iframe
                        src="https://www.youtube.com/embed/pOYq1aaJHRk?si=B2nBmp5UC2dI_p0I"
                        title="Entrevista al Presidente de Ecuador Daniel Noboa Azín"
                        frameborder="0"
                        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                        allowfullscreen
                        loading="lazy">
                    </iframe>
                </div>
                <p>Entrevista al Presidente de Ecuador Daniel Noboa Azín.</p>
                <div class="video-wrapper">
                    <iframe
                        src="https://www.youtube.com/embed/JReQmALQX4g?si=hhV0Z35AOG7uGafi"
                        title="Entrevista Exclusiva con Hernán Bravo Ordóñez"
                        frameborder="0"
                        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                        allowfullscreen
                        loading="lazy">
                    </iframe>
                </div>
                <p>El analista Hernán Bravo Ordóñez analiza la posibilidad de más apagones en Ecuador.</p>
            </div>
        </section>

        <!-- TV Play -->
        <section id="tvplay" class="section">
            <h2>TV Play</h2>
            <div class="grid">
                <div class="card">
                    <iframe width="100%" height="150" src="https://www.youtube.com/embed/xc4BXbdbPgk?si=jCPAkkJu3cfYakvQ" title="Programa Estelar de Milenium Tvi" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen loading="lazy"></iframe>
                    <div class="card-content">
                        <h3>Programa Estelar</h3>
                        <p>Disfruta de nuestro programa insignia con invitados especiales.</p>
                    </div>
                </div>
                <div class="card">
                    <iframe width="100%" height="150" src="https://www.youtube.com/embed/QRV5teEvBlY?si=21Sz5Mp5ZkxKiV1W" title="Serie Exclusiva de Milenium Tvi" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen loading="lazy"></iframe>
                    <div class="card-content">
                        <h3>Serie Exclusiva</h3>
                        <p>Una serie que no te puedes perder, disponible en TV Play.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Noticias -->
        <section id="news" class="section">
            <h2>Noticias</h2>
            <div class="grid">
                <div class="card">
                    <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/cooperativa-crea.jpg" alt="Suspensión de operaciones de la Cooperativa CREA Ltda." loading="lazy">
                    <div class="card-content">
                        <h3>Suspensión de operaciones de la Cooperativa CREA Ltda.</h3>
                        <p>La SEPS dispone la suspensión de operaciones y liquidación forzosa de la Cooperativa CREA Ltda.</p>
                        <a href="https://mileniumtvi.com/suspension-de-operaciones-y-liquidacion-forzosa-de-la-cooperativa-crea-ltda" target="_blank">Leer más</a>
                    </div>
                </div>
                <div class="card">
                    <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/jovenes-accion.jpg" alt="Programa Jóvenes en Acción" loading="lazy">
                    <div class="card-content">
                        <h3>Jóvenes en Acción abrirá plazas de empleo</h3>
                        <p>El programa Jóvenes en Acción abrirá oportunidades laborales para 80,000 personas.</p>
                        <a href="https://mileniumtvi.com/jovenes-en-accion-abrira-plazas-de-empleo-para-80-mil-personas-mas" target="_blank">Leer más</a>
                    </div>
                </div>
                <div class="card">
                    <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/noboa-guayaquil.jpg" alt="Presidente Noboa en Guayaquil" loading="lazy">
                    <div class="card-content">
                        <h3>Presidente Noboa honra a Guayaquil</h3>
                        <p>Daniel Noboa celebró los 490 años de fundación de Guayaquil.</p>
                        <a href="https://mileniumtvi.com/el-presidente-noboa-honro-a-la-perla-del-pacifico-en-sus-490-anios-de-fundacion" target="_blank">Leer más</a>
                    </div>
                </div>
                <div class="card">
                    <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/guayaquil-490.jpg" alt="Celebración de los 490 años de Guayaquil" loading="lazy">
                    <div class="card-content">
                        <h3>490 años de Guayaquil</h3>
                        <p>Guayaquil celebra sus 490 años con eventos culturales y desfiles.</p>
                        <a href="https://mileniumtvi.com/490-anios-de-guayaquil" target="_blank">Leer más</a>
                    </div>
                </div>
                <!-- Nota: Agrega más tarjetas con imágenes únicas -->
            </div>
        </section>

        <!-- Noticias Locales -->
        <section id="locales" class="section">
            <h2>Noticias Locales</h2>
            <div class="grid">
                <div class="card">
                    <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/cumbe-lote.jpg" alt="Cumbe participa en ordenanza de lote mínimo" loading="lazy">
                    <div class="card-content">
                        <h3>Cumbe aporta a la ordenanza del lote mínimo</h3>
                        <p>Cumbe contribuye a la construcción participativa de la ordenanza del lote mínimo.</p>
                        <a href="https://mileniumtvi.com/cumbe-aporto-a-la-construccion-participativa-del-lote-minimo" target="_blank">Leer más</a>
                    </div>
                </div>
                <div class="card">
                    <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/cuenca-segura.jpg" alt="Cuenca, ciudad más segura de Sudamérica" loading="lazy">
                    <div class="card-content">
                        <h3>Cuenca, la ciudad más segura de Sudamérica</h3>
                        <p>Cuenca es reconocida por Numbeo como la ciudad más segura de Sudamérica.</p>
                        <a href="https://mileniumtvi.com/cuenca-ciudad-mas-segura-de-sudamerica-segun-numbeo" target="_blank">Leer más</a>
                    </div>
                </div>
                <!-- Nota: Agrega más tarjetas con imágenes únicas -->
            </div>
        </section>

        <!-- Noticia en Imágenes -->
        <section id="imagenes" class="section">
            <h2>Noticia en Imágenes</h2>
            <div class="grid">
                <div class="card">
                    <img src="https://img.youtube.com/vi/3Ws3KFTv4pE/hqdefault.jpg" alt="Distribuidor de Tráfico Monay - ÍESS en Azuay" loading="lazy">
                    <div class="card-content">
                        <h3>Distribuidor de Tráfico Monay - ÍESS</h3>
                        <p>Daniel Noboa lideró la colocación de la primera piedra del distribuidor en Azuay, 30 de julio de 2025.</p>
                        <a href="https://youtu.be/3Ws3KFTv4pE" target="_blank">Ver video</a>
                    </div>
                </div>
                <div class="card">
                    <img src="https://img.youtube.com/vi/z1xQfEvFjA8/hqdefault.jpg" alt="Inauguración Central Termoeléctrica El Descanso II" loading="lazy">
                    <div class="card-content">
                        <h3>Inauguración Central Termoeléctrica</h3>
                        <p>El presidente Noboa inauguró la Central Termoeléctrica El Descanso II en Cañar.</p>
                        <a href="https://youtu.be/z1xQfEvFjA8?si=deueu9QrihN2rcYY" target="_blank">Ver video</a>
                    </div>
                </div>
                <div class="card">
                    <img src="https://img.youtube.com/vi/z77l-H4H664/hqdefault.jpg" alt="Accidente en Cuenca - Girón - Pasaje" loading="lazy">
                    <div class="card-content">
                        <h3>Accidente en Cuenca - Girón - Pasaje</h3>
                        <p>Dos personas fallecieron en un accidente de tránsito en la vía Cuenca - Girón - Pasaje.</p>
                        <a href="https://youtu.be/z77l-H4H664?si=Ey-LekZGWl7tz1-D" target="_blank">Ver video</a>
                    </div>
                </div>
            </div>
        </section>

        <!-- Videos -->
        <section id="videos" class="section">
            <h2>Videos</h2>
            <div class="grid">
                <div class="card">
                    <iframe width="100%" height="150" src="https://www.youtube.com/embed/MHjAUKw1VAE" title="Video Viral de Milenium Tvi" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen loading="lazy"></iframe>
                    <div class="card-content">
                        <h3>Video Viral</h3>
                        <p>Mira los videos más populares de la semana.</p>
                    </div>
                </div>
                <div class="card">
                    <iframe width="100%" height="150" src="https://www.youtube.com/embed/WIc2_BaF0Mo?si=GMguO6tXNOpN9GYc" title="Entrevista Exclusiva de Milenium Tvi" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen loading="lazy"></iframe>
                    <div class="card-content">
                        <h3>Entrevista Exclusiva</h3>
                        <p>Una charla con una celebridad que no te puedes perder.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Publicaciones -->
        <section id="posts" class="section">
            <h2>Publicaciones</h2>
            <div class="grid">
                <div class="card">
                    <a href="https://mileniumtvi.com/mas-de-100-ciudadanos-de-perucho-se-certifican-en-herramientas-digitales-y-rompen-la-brecha-tecnologica">
                        <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/perucho-digital.jpg" alt="Transformación Digital en Perucho" loading="lazy">
                    </a>
                    <div class="card-content">
                        <h3>Transformación Digital en Perucho</h3>
                        <p>Más de 100 ciudadanos de Perucho se certifican en herramientas digitales.</p>
                        <a href="https://mileniumtvi.com/mas-de-100-ciudadanos-de-perucho-se-certifican-en-herramientas-digitales-y-rompen-la-brecha-tecnologica">Leer más</a>
                    </div>
                </div>
                <div class="card">
                    <a href="https://mileniumtvi.com/el-80--de-las-enfermedades-cronicas-se-pueden-prevenir-con-autocuidadopor-ciento-">
                        <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/salud-preventiva.jpg" alt="Prevención de enfermedades crónicas" loading="lazy">
                    </a>
                    <div class="card-content">
                        <h3>80% de enfermedades crónicas prevenibles</h3>
                        <p>Expertos destacan que el autocuidado puede prevenir el 80% de las enfermedades crónicas.</p>
                        <a href="https://mileniumtvi.com/el-80--de-las-enfermedades-cronicas-se-pueden-prevenir-con-autocuidadopor-ciento-">Leer más</a>
                    </div>
                </div>
                <div class="card">
                    <a href="https://mileniumtvi.com/jose-adolfo-fito-macias-villamar-lider-de-la-organizacion-criminal-transnacional-los-choneros-fue-extraditado">
                        <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/fito-macias.jpg" alt="Extradición de Fito Macías" loading="lazy">
                    </a>
                    <div class="card-content">
                        <h3>Extradición de Fito Macías</h3>
                        <p>José Adolfo Fito Macías, líder de Los Choneros, fue extraditado.</p>
                        <a href="https://mileniumtvi.com/jose-adolfo-fito-macias-villamar-lider-de-la-organizacion-criminal-transnacional-los-choneros-fue-extraditado">Leer más</a>
                    </div>
                </div>
                <div class="card">
                    <a href="https://mileniumtvi.com/ecuador-y-emiratos-arabes-unidos-fortalecen-lazos-de-cooperacion">
                        <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/ecuador-emiratos.jpg" alt="Relaciones Ecuador-Emiratos Árabes Unidos" loading="lazy">
                    </a>
                    <div class="card-content">
                        <h3>Artículo Especial</h3>
                        <p>Ecuador y Emiratos Árabes Unidos firman acuerdos para impulsar turismo y seguridad.</p>
                        <a href="https://mileniumtvi.com/ecuador-y-emiratos-arabes-unidos-fortalecen-lazos-de-cooperacion">Leer más</a>
                    </div>
                </div>
                <!-- Nota: Agrega más tarjetas con imágenes únicas -->
            </div>
        </section>

        <!-- Defensa del Televidente -->
        <section id="defensa" class="section">
            <h2>Defensa del Televidente</h2>
            <p>Tu voz importa. Contáctanos para cualquier queja, sugerencia o consulta.</p>
            <form action="https://formspree.io/f/your-form-id" method="POST" aria-label="Formulario de contacto">
                <div class="form-group">
                    <label for="name">Nombre</label>
                    <input type="text" id="name" name="name" placeholder="Nombre" required aria-required="true">
                </div>
                <div class="form-group">
                    <label for="email">Correo Electrónico</label>
                    <input type="email" id="email" name="email" placeholder="Correo Electrónico" required aria-required="true">
                </div>
                <div class="form-group">
                    <label for="message">Mensaje</label>
                    <textarea id="message" name="message" placeholder="Tu mensaje" required aria-required="true"></textarea>
                </div>
                <div class="form-group honeypot">
                    <label for="honeypot">No llenes este campo si eres humano</label>
                    <input type="text" id="honeypot" name="honeypot">
                </div>
                <div class="form-group">
                    <button type="submit">Enviar</button>
                </div>
            </form>
        </section>
    </main>

    <!-- Footer -->
    <footer role="contentinfo">
        <p>© 2025 Milenium Tvi. Todos los derechos reservados.</p>
        <p>
            <a href="#">Términos y Condiciones</a> | 
            <a href="#">Política de Privacidad</a> | 
            <a href="#defensa">Contacto</a>
        </p>
        <div class="social">
            <a href="https://www.facebook.com/mileniumtvi/" target="_blank" aria-label="Facebook de Milenium Tvi"><i class="fab fa-facebook-f"></i></a>
            <a href="https://x.com/mileniumtvi" target="_blank" aria-label="X de Milenium Tvi"><i class="fab fa-x-twitter"></i></a>
            <a href="https://www.instagram.com/mileniumtvi/" target="_blank" aria-label="Instagram de Milenium Tvi"><i class="fab fa-instagram"></i></a>
            <a href="https://www.youtube.com/@mileniumtvi" target="_blank" aria-label="YouTube de Milenium Tvi"><i class="fab fa-youtube"></i></a>
        </div>
    </footer>

    <!-- Back to Top Button -->
    <button class="back-to-top" aria-label="Volver arriba"><i class="fas fa-arrow-up"></i></button>

    <!-- Video.js Script -->
    <script src="https://vjs.zencdn.net/8.10.0/video.min.js"></script>
    <script>
        // Smooth scroll para los enlaces de navegación
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Menú hamburguesa
        const menuToggle = document.querySelector('.menu-toggle');
        const navMenu = document.querySelector('nav ul');
        menuToggle.addEventListener('click', () => {
            navMenu.classList.toggle('show');
            const expanded = navMenu.classList.contains('show');
            menuToggle.setAttribute('aria-expanded', expanded);
            menuToggle.innerHTML = expanded ? '<i class="fas fa-times"></i>' : '<i class="fas fa-bars"></i>';
        });

        // Botón Volver arriba
        const backToTop = document.querySelector('.back-to-top');
        window.addEventListener('scroll', () => {
            if (window.scrollY > 300) {
                backToTop.classList.add('show');
            } else {
                backToTop.classList.remove('show');
            }
        });
        backToTop.addEventListener('click', () => {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        });
    </script>
</body>
</html>

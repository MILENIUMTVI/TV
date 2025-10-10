<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Página oficial de Milenium Tvi: transmisiones en vivo, noticias, videos y entretenimiento en Ecuador.">
    <meta name="keywords" content="noticias Ecuador, TV en vivo, Milenium Tvi, Daniel Noboa, entrevistas, series, películas">
    <meta property="og:title" content="Milenium Tvi: Noticias, Transmisiones en Vivo y Entretenimiento en Ecuador">
    <meta property="og:description" content="Tu fuente de entretenimiento, noticias y mucho más en Milenium Tvi.">
    <meta property="og:image" content="https://mileniumtvi.com/logo.png"> <!-- Reemplaza con imagen real -->
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
            gap: 0.8rem; /* Reducido para mejor balance */
            align-items: center;
            flex-wrap: wrap;
            justify-content: center; /* Centra los ítems del menú */
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
            background: url('https://mileniumtvi.com/banner-hero.jpg') no-repeat center/cover; /* Reemplaza con imagen real */
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
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="header-container">
            <div class="logo">
                <img src="https://mileniumtvi.com/logo.png" alt="Logo de Milenium Tvi"> <!-- Reemplaza con src real -->
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

    <!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Transmisiones en Vivo</title>
    <!-- Estilos de Video.js (asegúrate de incluir la biblioteca) -->
    <link href="https://vjs.zencdn.net/8.10.0/video-js.css" rel="stylesheet" />
    <!-- Estilos personalizados para responsividad -->
    <style>
        .section.live-stream {
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .entrevistas-container {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .video-wrapper {
            position: relative;
            width: 100%;
            max-width: 800px; /* Limita el ancho máximo en pantallas grandes */
            margin: 0 auto;
            aspect-ratio: 16 / 9; /* Mantiene la relación de aspecto del video */
        }

        .video-wrapper video {
            width: 100%;
            height: 100%;
            object-fit: contain; /* Asegura que el video no se distorsione */
        }

        .entrevistas-container p {
            text-align: center;
            font-size: 1rem;
            margin: 10px 0;
            color: #333;
        }

        /* Ajustes para pantallas pequeñas */
        @media screen and (max-width: 600px) {
            .section.live-stream {
                padding: 10px;
            }

            .video-wrapper {
                max-width: 100%;
            }

            .entrevistas-container p {
                font-size: 0.9rem;
            }
        }
    </style>
</head>
<body>
   <!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Transmisiones en Vivo</title>
    <!-- Estilos de Video.js -->
    <link href="https://vjs.zencdn.net/8.10.0/video-js.css" rel="stylesheet" />
    <!-- Estilos personalizados para responsividad -->
    <style>
        .section.live-stream {
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .entrevistas-container {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .video-wrapper {
            position: relative;
            width: 100%;
            max-width: 800px; /* Limita el ancho máximo en pantallas grandes */
            margin: 0 auto;
            overflow: hidden; /* Evita desbordamientos */
        }

        /* Asegurar que el video mantenga la relación de aspecto y se ajuste al contenedor */
        .video-wrapper .vjs-tech {
            width: 100%;
            height: auto;
            aspect-ratio: 16 / 9;
            object-fit: contain; /* Evita recortes o distorsiones */
        }

        /* Ajustar el contenedor de Video.js para ser responsivo */
        .video-js {
            width: 100%;
            height: auto;
            aspect-ratio: 16 / 9;
        }

        /* Estilos para el texto descriptivo */
        .entrevistas-container p {
            text-align: center;
            font-size: 1rem;
            margin: 10px 0;
            color: #333;
        }

        /* Ajustes para pantallas pequeñas */
        @media screen and (max-width: 600px) {
            .section.live-stream {
                padding: 10px;
            }

            .video-wrapper {
                max-width: 100%;
            }

            .entrevistas-container p {
                font-size: 0.9rem;
            }

            /* Forzar que el video sea completamente visible en móviles */
            .video-js, .video-wrapper .vjs-tech {
                width: 100% !important;
                height: auto !important;
                max-height: 50vh; /* Limita la altura máxima para evitar desbordes */
            }
        }
    </style>
</head>
<body>
    <!-- Transmisiones en Vivo -->
    <section id="live" class="section live-stream">
        <h2>Transmisiones en Vivo</h2>
        <div class="entrevistas-container">
            <div class="video-wrapper">
                <video id="live-stream-player-1" class="video-js vjs-default-skin" controls preload="auto" data-setup='{"fluid": true, "aspectRatio": "16:9", "responsive": true}'>
                    <source src="https://app.viloud.tv/hls/channel/c8984eee3163b175a0c725860f53749d.m3u8" type="application/x-mpegURL">
                    <p class="vjs-no-js">
                        Para ver este video, habilita JavaScript y considera actualizar a un navegador que soporte video HTML5.
                    </p>
                </video>
            </div>
            <p>Transmisión en vivo del canal principal de Milenium Tvi.</p>
            <div class="video-wrapper">
                <video id="live-stream-player-2" class="video-js vjs-default-skin" controls preload="auto" data-setup='{"fluid": true, "aspectRatio": "16:9", "responsive": true}'>
                    <source src="https://app.viloud.tv/hls/channel/119c56a41cef4bf9b47e6d600cc70a63.m3u8" type="application/x-mpegURL">
                    <p class="vjs-no-js">
                        Para ver este video, habilita JavaScript y considera actualizar a un navegador que soporte video HTML5.
                    </p>
                </video>
            </div>
            <p>Disfruta de la mejor selección de música en vivo con MTVI2 Musical.</p>
            <div class="video-wrapper">
                <video id="live-stream-player-3" class="video-js vjs-default-skin" controls preload="auto" data-setup='{"fluid": true, "aspectRatio": "16:9", "responsive": true}'>
                    <source src="https://app.viloud.tv/hls/channel/fa28724c715bb373296ca57a2dcd551c.m3u8" type="application/x-mpegURL">
                    <p class="vjs-no-js">
                        Para ver este video, habilita JavaScript y considera actualizar a un navegador que soporte video HTML5.
                    </p>
                </video>
            </div>
            <p>Las mejores películas en streaming continuo con MTVI3 Películas.</p>
            <div class="video-wrapper">
                <video id="live-stream-player-4" class="video-js vjs-default-skin" controls preload="auto" data-setup='{"fluid": true, "aspectRatio": "16:9", "responsive": true}'>
                    <source src="https://app.viloud.tv/hls/channel/8823313f19b20ef55dea4f3ad8a4cab7.m3u8" type="application/x-mpegURL">
                    <p class="vjs-no-js">
                        Para ver este video, habilita JavaScript y considera actualizar a un navegador que soporte video HTML5.
                    </p>
                </video>
            </div>
            <p>Tus series favoritas en transmisión en vivo con MTVI4 Series.</p>
        </div>
    </section>

    <!-- Incluir el script de Video.js -->
    <script src="https://vjs.zencdn.net/8.10.0/video.min.js"></script>
    <!-- Inicialización manual de Video.js para mayor control -->
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Inicializar cada reproductor de video
            const players = [
                'live-stream-player-1',
                'live-stream-player-2',
                'live-stream-player-3',
                'live-stream-player-4'
            ];

            players.forEach(playerId => {
                videojs(playerId, {
                    fluid: true,
                    responsive: true,
                    aspectRatio: '16:9',
                    playbackRates: [0.5, 1, 1.5, 2], // Opcional: agregar opciones de velocidad
                    controlBar: {
                        volumePanel: { inline: false } // Ajustar controles para móviles
                    }
                });
            });
        });
    </script>
</body>
</html>

   <!-- TV Play -->
<section id="tvplay" class="section">
    <h2>TV Play</h2>
    <div class="grid">
        <div class="card">
            <iframe loading="lazy" width="100%" height="315" src="https://www.youtube.com/embed/S-YnJOWrnm4?si=YRWN26E69KDaoesF" title="Ecos bajo la piel" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            <div class="card-content">
                <h3>Ecos bajo la piel</h3>
                <p>Isis Patiño, productora y creadora de la obra "Ecos bajo la piel", Directora del colectivo escénico Raíz en Movimiento y Cofundadora de la Escuela de Artes Escénicas Medicina.</p>
            </div>
        </div>
        <div class="card">
            <iframe loading="lazy" width="100%" height="315" src="https://www.youtube.com/embed/iaSi9DRFx9c?si=noTdteZj20HH5UJV" title="Funky Night con Da Grove Jazz Music Project" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            <div class="card-content">
                <h3>Funky Night con Da Grove Jazz Music Project</h3>
                <p>Alicia Boroto Directora del Centro Abraham Lincoln y Verónica Coello Directora Cultural del CEN invitan al Evento Gratuito FUNKY NIGHT CON DA GROVE JAZZ MUSIC PROJECT que será el jueves 16 de octubre desde las 19h30 en el Auditorio del Centro Abraham Lincoln en Borrero y Honorato Vázquez</p>
            </div>
        </div>
        <div class="card">
            <iframe loading="lazy" width="100%" height="315" src="https://www.youtube.com/embed/xc4BXbdbPgk" title="Programa Estelar" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            <div class="card-content">
                <h3>Programa Estelar</h3>
                <p>Disfruta de nuestro programa insignia con invitados especiales.</p>
            </div>
        </div>
        <div class="card">
            <iframe loading="lazy" width="100%" height="315" src="https://www.youtube.com/embed/QRV5teEvBlY" title="Serie Exclusiva" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            <div class="card-content">
                <h3>Serie Exclusiva</h3>
                <p>Una serie que no te puedes perder, disponible en TV Play.</p>
            </div>
        </div>
    </div>
</section>

<!-- Transmisión Alternativa -->
<section id="alternative-stream" class="section live-stream">
    <h2>Transmisión Alternativa</h2>
    <div class="entrevistas-container">
        <div class="video-wrapper">
            <div style='position: relative; padding-bottom: 56.25%; height: 0;'>
                <iframe src='https://player.viloud.tv/embed/channel/c8984eee3163b175a0c725860f53749d?autoplay=0&volume=1&controls=1&title=1&share=1&open_playlist=0&random=0' style='position: absolute; top: 0; left: 0; width: 100%; height: 100%;' frameborder='0' allow='autoplay' allowfullscreen></iframe>
            </div>
        </div>
        <p>Transmisión alternativa del canal principal de Milenium Tvi.</p>
    </div>
</section>

<!-- Estilos para consistencia visual -->
<style>
    .section.live-stream {
        margin: 2rem 0;
    }
    .entrevistas-container {
        max-width: 1200px;
        margin: 0 auto;
        padding: 0 1rem;
    }
    .video-wrapper {
        max-width: 100%;
        margin-bottom: 1rem;
    }
    .video-wrapper iframe {
        border: none;
        border-radius: 8px; /* Opcional: para consistencia con Video.js */
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); /* Opcional: sombra para mejor estética */
    }
    h2 {
        text-align: center;
        margin-bottom: 1.5rem;
    }
</style>
  
<!-- Noticias -->
<section id="news" class="section">
    <h2>Noticias</h2>
    <div class="grid">
        <div class="card">
            <div class="card-content">
                <h3>El Gobierno del presidente Daniel Noboa implementa la tecnología 5G, impulsando la transformación digital del Ecuador</h3>
                <p>El Gobierno del presidente Daniel Noboa implementa la tecnología 5G, impulsando la transformación digital del Ecuador, mejorando la conectividad y fomentando la innovación en el país.</p>
                <a href="https://mileniumtvi.com/el-gobierno-del-presidente-daniel-noboa-implementa-la-tecnologia-5g-impulsando-la-transformacion-digital-del-ecuador" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>El Gobierno del nuevo Ecuador certificó a 300 jóvenes de Calacalí en el manejo de herramientas tecnológicas y redes sociales</h3>
                <p>El Gobierno del nuevo Ecuador certificó a 300 jóvenes de Calacalí en el manejo de herramientas tecnológicas y redes sociales, impulsando sus habilidades digitales para el futuro.</p>
                <a href="https://mileniumtvi.com/el-gobierno-del-nuevo-ecuador-certifico-a-300-jovenes-de-calacali-en-el-manejo-de-herramientas-tecnologicas-y-redes-sociales" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Ecuador amplía la Reserva de Biosfera Galápagos con la inclusión de la Reserva Marina Hermandad</h3>
                <p>Ecuador amplía la Reserva de Biosfera Galápagos al incorporar la Reserva Marina Hermandad, fortaleciendo la conservación de este ecosistema único.</p>
                <a href="https://mileniumtvi.com/ecuador-amplia-la-reserva-de-biosfera-galapagos-con-la-inclusion-de-la-reserva-marina-hermandad" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>En Cuenca, el concierto Funky Night</h3>
                <p>Cuenca vibró con el concierto Funky Night, un evento que reunió a amantes de la música en una noche llena de ritmo y energía.</p>
                <a href="https://mileniumtvi.com/en-cuenca-el-concierto-funky-night" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>El Gobierno Nacional celebra la Independencia de Guayaquil con más oportunidades digitales para sus ciudadanos</h3>
                <p>El Gobierno Nacional conmemora la Independencia de Guayaquil impulsando oportunidades digitales para mejorar la conectividad y el acceso a la tecnología.</p>
                <a href="https://mileniumtvi.com/el-gobierno-nacional-celebra-la-independencia-de-guayaquil-con-mas-oportunidades-digitales-para-sus-ciudadanos" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Puntos Digitales Gratuitos PDG 9 de Octubre y El Astillero</h3>
                <p>Se inauguran puntos digitales gratuitos en 9 de Octubre y El Astillero, mejorando el acceso a internet y la conectividad en estas comunidades.</p>
                <a href="https://mileniumtvi.com/puntos-digitales-gratuitos-pdg-9-de-octubre-y-el-astillero" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>La vicepresidenta María José Pinto supervisa servicios a la primera infancia y de salud en Cayambe</h3>
                <p>La vicepresidenta María José Pinto supervisa programas de atención a la primera infancia y servicios de salud en Cayambe, garantizando su calidad y acceso.</p>
                <a href="https://mileniumtvi.com/la-vicepresidenta-maria-jose-pinto-supervisa-servicios-a-la-primera-infancia-y-de-salud-en-cayambe" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>El fraude digital se dispara: reseñas falsas y bots ponen en jaque al e-commerce global</h3>
                <p>El aumento de reseñas falsas y bots representa un desafío para el comercio electrónico global, afectando la confianza de los consumidores.</p>
                <a href="https://mileniumtvi.com/el-fraude-digital-se-dispara-resenas-falsas-y-bots-ponen-en-jaque-al-e-commerce-global" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Gobierno intensifica operativos para garantizar abastecimiento y evitar especulación de combustibles y gas en todo el país</h3>
                <p>El gobierno intensifica operativos para asegurar el abastecimiento de combustibles y gas, combatiendo la especulación en todo el territorio nacional.</p>
                <a href="https://mileniumtvi.com/gobierno-intensifica-operativos-para-garantizar-abastecimiento-y-evitar-especulacion-de-combustibles-y-gas-en-todo-el-pais" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>CONADIS y Ministerio del Trabajo establecen el nuevo perfil para certificar a intérpretes en lengua de señas ecuatoriana</h3>
                <p>CONADIS y el Ministerio del Trabajo definen un nuevo perfil para certificar intérpretes en lengua de señas, promoviendo la inclusión de personas con discapacidad auditiva.</p>
                <a href="https://mileniumtvi.com/conadis-y-ministerio-del-trabajo-establecen-el-nuevo-perfil-para-certificar-a-interpretes-en-lengua-de-senas-ecuatoriana-conadis-y-ministerio-del-trabajo-establecen-el-nuevo-perfil-para-certificar-a-interpretes-en-lengua-de-senas-ecuatoriana" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>María José Pinto fortalece apoyo a la niñez y juventud en situación de riesgo en Ibarra</h3>
                <p>La vicepresidenta María José Pinto impulsa iniciativas para proteger y apoyar a la niñez y juventud en situación de riesgo en Ibarra, promoviendo su bienestar y desarrollo.</p>
                <a href="https://mileniumtvi.com/maria-jose-pinto-fortalece-apoyo-a-la-ninez-y-juventud-en-situacion-de-riesgo-en-ibarra" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Ventas en Ecuador crecen en septiembre pese a focalizados intentos de paralización</h3>
                <p>Las ventas en Ecuador registraron un crecimiento en septiembre, superando intentos focalizados de paralización, impulsando la economía local.</p>
                <a href="https://mileniumtvi.com/ventas-en-ecuador-crecen-en-septiembre-pese-a-focalizados-intentos-de-paralizacion" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>La vida cambió para doña María con la adecuación de su vivienda y acceso a servicios básicos</h3>
                <p>Doña María mejora su calidad de vida gracias a la adecuación de su vivienda y el acceso a servicios básicos, como parte de iniciativas sociales en Ecuador.</p>
                <a href="https://mileniumtvi.com/la-vida-cambio-para-dona-maria-con-la-adecuacion-de-su-vivienda-y-acceso-a-servicios-basicos" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>“Nadie nos va a impedir llegar a las comunidades”: presidente Noboa entregó créditos y herramientas para Imbabura</h3>
                <p>El presidente Daniel Noboa entregó créditos y herramientas a comunidades de Imbabura, reafirmando su compromiso con el desarrollo local.</p>
                <a href="https://mileniumtvi.com/nadie-nos-va-a-impedir-llegar-a-las-comunidades-presidente-noboa-entrego-creditos-y-herramientas-para-imbabura" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Agricultores de Tungurahua recibieron bonos Raíces y otros insumos productivos, en todo el país ya son más de 81,000 beneficiarios</h3>
                <p>Agricultores de Tungurahua reciben bonos Raíces e insumos productivos, sumándose a los más de 81,000 beneficiarios a nivel nacional.</p>
                <a href="https://mileniumtvi.com/agricultores-de-tungurahua-recibieron-bonos-raices-y-otros-insumos-productivos-en-todo-el-pais-ya-son-mas-de-81000-beneficiarios" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Presidente Daniel Noboa entrega USD 6 millones para la economía popular y solidaria de Tungurahua</h3>
                <p>El presidente Daniel Noboa destinó USD 6 millones para fortalecer la economía popular y solidaria en Tungurahua, apoyando a emprendedores locales.</p>
                <a href="https://mileniumtvi.com/presidente-daniel-noboa-entrega-usd-6-millones-para-la-economia-popular-y-solidaria-de-tungurahua" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Familias de Tungurahua cumplen su sueño de tener casa propia</h3>
                <p>Familias de Tungurahua logran tener casa propia gracias a programas del gobierno que promueven el acceso a viviendas dignas.</p>
                <a href="https://mileniumtvi.com/familias-de-tungurahua-cumplen-su-sueno-de-tener-casa-propia-" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Vicepresidenta María José Pinto promueve el trabajo conjunto por la educación intercultural bilingüe</h3>
                <p>La vicepresidenta María José Pinto impulsa iniciativas para fortalecer la educación intercultural bilingüe, promoviendo la inclusión y el respeto a la diversidad cultural en Ecuador.</p>
                <a href="https://mileniumtvi.com/vicepresidenta-maria-jose-pinto-promueve-el-trabajo-en-conjunto-y-articulado-por-la-educacion-intercultural-bilingue" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Desde Cotopaxi, el gobierno de Daniel Noboa entrega créditos productivos al sector turístico</h3>
                <p>En Cotopaxi, el gobierno de Daniel Noboa entrega créditos productivos para impulsar el turismo, apoyando el desarrollo económico y la generación de empleo en el sector.</p>
                <a href="https://mileniumtvi.com/desde-cotopaxi-el-gobierno-de-daniel-noboa-entrega-creditos-productivos-al-sector-turistico" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Carolina Jaramillo, portavoz de Carondelet</h3>
                <p>Carolina Jaramillo asume el rol de portavoz de Carondelet, fortaleciendo la comunicación oficial del gobierno ecuatoriano con transparencia y claridad.</p>
                <a href="https://mileniumtvi.com/carolina-jaramillo-portavoz-de-carondelet" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>“O aquí me quedo luchando todos los días por ustedes”</h3>
                <p>El presidente Daniel Noboa reafirma su compromiso con los ecuatorianos, destacando su dedicación diaria para mejorar la calidad de vida y enfrentar los desafíos del país.</p>
                <a href="https://mileniumtvi.com/o-aqui-me-quedo-luchando-todos-los-dias-por-ustedes" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Por primera vez, afiliados del Seguro Social Campesino reciben montepio</h3>
                <p>El presidente Daniel Noboa hace realidad el acceso al montepio para los afiliados del Seguro Social Campesino, garantizando beneficios para este sector vulnerable.</p>
                <a href="https://mileniumtvi.com/por-primera-vez-afiliados-del-seguro-social-campesino-reciben-montepio-daniel-noboa-hace-realidad-el-acceso-a-este-derecho" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>6000 estudiantes de centros educativos de la FAE cuentan con internet de calidad</h3>
                <p>6000 estudiantes de centros educativos de la FAE cuentan con internet de calidad, mejorando el acceso a recursos educativos y conectividad.</p>
                <a href="https://mileniumtvi.com/6000-estudiantes-de-centros-educativos-de-la-fae-cuenten-con-internet-de-calidad-" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>La Corte Constitucional del Ecuador emitió tres dictámenes relacionados con propuestas de enmienda constitucional, reforma parcial y consulta popular presentadas por el presidente de la República</h3>
                <p>La Corte Constitucional del Ecuador emitió tres dictámenes relacionados con propuestas de enmienda constitucional, reforma parcial y consulta popular presentadas por el presidente de la República.</p>
                <a href="https://mileniumtvi.com/la-corte-constitucional-del-ecuador-emitio-tres-dictamenes-relacionados-con-propuestas-de-enmienda-constitucional-reforma-parcial-y-consulta-popular-presentadas-por-el-presidente-de-la-republica" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>En entrevista con Univision, el presidente Noboa destacó la cooperación con EEUU en seguridad y lucha contra la minería ilegal</h3>
                <p>En entrevista con Univision, el presidente Noboa destacó la cooperación con EEUU en seguridad y lucha contra la minería ilegal.</p>
                <a href="https://mileniumtvi.com/en-entrevista-con-univision-el-presidente-noboa-destaco-la-cooperacion-con-eeuu-en-seguridad-y-lucha-contra-la-mineria-ilegal" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Pleno de Concejo Cantonal solicita que comisión sobre proyecto minero Loma Larga convocada por la asambleista Camila León se realice en Cuenca</h3>
                <p>Pleno de Concejo Cantonal solicita que comisión sobre proyecto minero Loma Larga convocada por la asambleista Camila León se realice en Cuenca.</p>
                <a href="https://mileniumtvi.com/pleno-de-concejo-cantonal-solicita-que-comision-sobre-proyecto-minero-loma-larga-convocada-por-la-asambleista-camila-leon-se-realice-en-cuenca" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>La Casa Blanca notificó oficialmente al Congreso sobre el ataque militar del 2 de septiembre en el Caribe y advirtió que podrían venir nuevas acciones</h3>
                <p>La Casa Blanca notificó oficialmente al Congreso sobre el ataque militar del 2 de septiembre en el Caribe y advirtió que podrían venir nuevas acciones.</p>
                <a href="https://mileniumtvi.com/la-casa-blanca-notifico-oficialmente-al-congreso-sobre-el-ataque-militar-del-2-de-septiembre-en-el-caribe-y-advirtio-que-podrian-venir-nuevas-acciones" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Si nos ponen en una situación peligrosa, serán derribados, advirtió el líder republicano horas después de anunciar el envío de 10 cazas F-35 a Puerto Rico</h3>
                <p>Si nos ponen en una situación peligrosa, serán derribados, advirtió el líder republicano horas después de anunciar el envío de 10 cazas F-35 a Puerto Rico.</p>
                <a href="https://mileniumtvi.com/si-nos-ponen-en-una-situacion-peligrosa-seran-derribados-advirtio-el-lider-republicano-horas-despues-de-anunciar-el-envio-de-10-cazas-f-35-a-puerto-rico" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>La Guardia Costera incauta 40000 libras de cocaína en el Pacífico y publica imágenes de las operaciones y del buque en llamas</h3>
                <p>La Guardia Costera incauta 40000 libras de cocaína en el Pacífico y publica imágenes de las operaciones y del buque en llamas.</p>
                <a href="https://mileniumtvi.com/la-guardia-costera-incauta-40000-libras-de-cocaina-en-el-pacifico-y-publica-imagenes-de-las-operaciones-y-del-buque-en-llamas" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Más niños, niñas y madres gestantes recibirán el bono de los 1000 días</h3>
                <p>Más niños, niñas y madres gestantes recibirán el bono de los 1000 días.</p>
                <a href="https://mileniumtvi.com/mas-ninos-ninas-y-madres-gestantes-recibiran-el-bono-de-los-1000-dias" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Marco Rubio, Secretario de Estado de Estados Unidos, visitó al Presidente Daniel Noboa en Carondelet</h3>
                <p>Marco Rubio, Secretario de Estado de Estados Unidos, visitó al Presidente Daniel Noboa en Carondelet.</p>
                <a href="https://mileniumtvi.com/marco-rubio-secretario-de-estado-de-estados-unidos-visito-al-presidente-daniel-noboa-en-carondelet" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Ecuador y Japón refuerzan la cooperación en energía, comercio, seguridad y gestión de riesgos</h3>
                <p>Ecuador y Japón refuerzan la cooperación en energía, comercio, seguridad y gestión de riesgos.</p>
                <a href="https://mileniumtvi.com/ecuador-y-japon-refuerzan-la-cooperacion-en-energia-comercio-seguridad-y-gestion-de-riesgos-" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
    </div>
</section>
</section>
</section>
</section>
```
<!-- Noticias Locales -->
<section id="locales" class="section">
    <h2>Noticias Locales</h2>
    <div class="grid">
        <div class="card">
            <a href="https://youtu.be/jlHFdHg4wfQ" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/jlHFdHg4wfQ/hqdefault.jpg" alt="Carolina Jaramillo sobre revocatoria de licencia ambiental">
            </a>
            <div class="card-content">
                <h3>Noticia Local</h3>
                <p>Carolina Jaramillo, Portavoz de Carondelet señala que el proceso de revocatoria de la licencia ambiental del proyecto Loma Larga de #Quimsacocha se basa en los informes técnicos presentados por el Alcalde de Cuenca y el Prefecto del Azuay, tienen gran responsabilidad y son ellos quienes tiene que dar respuesta a los ciudadanos cuencanos.</p>
                <a href="https://youtu.be/jlHFdHg4wfQ" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/cj6L7FsZrq0" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/cj6L7FsZrq0/hqdefault.jpg" alt="Yaku Pérez pide cancelación de concesiones mineras">
            </a>
            <div class="card-content">
                <h3>Noticia Local</h3>
                <p>El ex candidato presidencial y activista político Yaku Pérez ahora pide la cancelación de las 3 concesiones mineras, pues considera que la revocatoria de la licencia ambiental del proyecto Loma Larga ya no es suficiente.</p>
                <a href="https://youtu.be/cj6L7FsZrq0" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/_KcbM4rOls4" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/_KcbM4rOls4/hqdefault.jpg" alt="Verónica Polo sobre informes técnicos de ETAPA">
            </a>
            <div class="card-content">
                <h3>Noticia Local</h3>
                <p>Verónica Polo, Gerente de ETPA-EP, considera que los informes técnicos de ETAPA fueron fundamentales para la revocatoria de la licencia ambiental del proyecto minero Loma Larga en #Quimsacocha.</p>
                <a href="https://youtu.be/_KcbM4rOls4" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/VZKHW-K0898" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/VZKHW-K0898/hqdefault.jpg" alt="Alcalde Zamora sobre reversión de licencia">
            </a>
            <div class="card-content">
                <h3>Noticia Local</h3>
                <p>El Alcalde Zamora presentó los informes pero saca el cuerpo y no quiere responsabilizarse de la Reversión de Licencia del proyecto Loma Larga en #Quimsacocha.</p>
                <a href="https://youtu.be/VZKHW-K0898" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/9PsSY5SA9V4?si=03FcQynC4hqAFZ1f" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/9PsSY5SA9V4/hqdefault.jpg" alt="Noticia Local 1">
            </a>
            <div class="card-content">
                <h3>Noticia Local</h3>
                <p>Resumen de la noticia local presentada en el video, destacando eventos relevantes en la comunidad.</p>
                <a href="https://youtu.be/9PsSY5SA9V4?si=03FcQynC4hqAFZ1f" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/Guk-_LJJTEU?si=kxYj9qfsoKKEcvUw" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/Guk-_LJJTEU/hqdefault.jpg" alt="Noticia Local 2">
            </a>
            <div class="card-content">
                <h3>Noticia Local</h3>
                <p>Resumen de la noticia local presentada en el video, destacando eventos relevantes en la comunidad.</p>
                <a href="https://youtu.be/Guk-_LJJTEU?si=kxYj9qfsoKKEcvUw" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/QJxopt6Xc5E?si=1Ot-KUKEb3eC2h1R" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/QJxopt6Xc5E/hqdefault.jpg" alt="Noticia Local 3">
            </a>
            <div class="card-content">
                <h3>Noticia Local</h3>
                <p>Resumen de la noticia local presentada en el video, destacando eventos relevantes en la comunidad.</p>
                <a href="https://youtu.be/QJxopt6Xc5E?si=1Ot-KUKEb3eC2h1R" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/fkma9cZBj1g?si=BLtj8Zqf3hNTEJQU" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/fkma9cZBj1g/hqdefault.jpg" alt="Noticia Local 4">
            </a>
            <div class="card-content">
                <h3>Noticia Local</h3>
                <p>Resumen de la noticia local presentada en el video, destacando eventos relevantes en la comunidad.</p>
                <a href="https://youtu.be/fkma9cZBj1g?si=BLtj8Zqf3hNTEJQU" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/gpW-OMfAoYI?si=xZaJ3yW3VDlHaG-W" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/gpW-OMfAoYI/hqdefault.jpg" alt="Noticia Local 5">
            </a>
            <div class="card-content">
                <h3>Noticia Local</h3>
                <p>Resumen de la noticia local presentada en el video, destacando eventos relevantes en la comunidad.</p>
                <a href="https://youtu.be/gpW-OMfAoYI?si=xZaJ3yW3VDlHaG-W" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/ZzBVgyFuWM8?si=e6tUJZAme5fSKy7A" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/ZzBVgyFuWM8/hqdefault.jpg" alt="Noticia Local 6">
            </a>
            <div class="card-content">
                <h3>Noticia Local</h3>
                <p>Resumen de la noticia local presentada en el video, destacando eventos relevantes en la comunidad.</p>
                <a href="https://youtu.be/ZzBVgyFuWM8?si=e6tUJZAme5fSKy7A" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/fw3rIuhASac?si=1AYrmPsP6mIG_W_b" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/fw3rIuhASac/hqdefault.jpg" alt="Noticia Local 7">
            </a>
            <div class="card-content">
                <h3>Noticia Local</h3>
                <p>Resumen de la noticia local presentada en el video, destacando eventos relevantes en la comunidad.</p>
                <a href="https://youtu.be/fw3rIuhASac?si=1AYrmPsP6mIG_W_b" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/UXqluCrkDt0?si=c1CGc5NRxIh4lJ7d" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/UXqluCrkDt0/hqdefault.jpg" alt="Noticia Local 8">
            </a>
            <div class="card-content">
                <h3>Noticia Local</h3>
                <p>Resumen de la noticia local presentada en el video, destacando eventos relevantes en la comunidad.</p>
                <a href="https://youtu.be/UXqluCrkDt0?si=c1CGc5NRxIh4lJ7d" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/3n5YdEeS8Yc?si=KBE2zeyY76XoWwk2" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/3n5YdEeS8Yc/hqdefault.jpg" alt="Noticia Local 9">
            </a>
            <div class="card-content">
                <h3>Noticia Local</h3>
                <p>Resumen de la noticia local presentada en el video, destacando eventos relevantes en la comunidad.</p>
                <a href="https://youtu.be/3n5YdEeS8Yc?si=KBE2zeyY76XoWwk2" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://mileniumtvi.com/el-alcalde-de-latinoamerica" rel="noopener noreferrer">
                <img loading="lazy" src="https://via.placeholder.com/250x150" alt="Reconocimiento al Alcalde de Latinoamérica">
            </a>
            <div class="card-content">
                <h3>El Alcalde de Latinoamérica</h3>
                <p>Un reconocimiento al liderazgo regional en la gestión municipal, destacando iniciativas que transforman comunidades en América Latina.</p>
                <a href="https://mileniumtvi.com/el-alcalde-de-latinoamerica" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <a href="https://mileniumtvi.com/el-cacao-ecuatoriano-brilla-en-el-salon-del-chocolate-de-paris" rel="noopener noreferrer">
                <img loading="lazy" src="https://via.placeholder.com/250x150" alt="Cacao ecuatoriano destacando en Salón del Chocolate de París">
            </a>
            <div class="card-content">
                <h3>El cacao ecuatoriano brilla en el Salón del Chocolate de París</h3>
                <p>El cacao ecuatoriano destacó en el Salón del Chocolate de París, recibiendo reconocimientos por su calidad y sostenibilidad, consolidando a Ecuador como líder en el mercado global.</p>
                <a href="https://mileniumtvi.com/el-cacao-ecuatoriano-brilla-en-el-salon-del-chocolate-de-paris" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <img loading="lazy" src="https://mileniumtvi.com/wp-content/uploads/2025/07/Bloque-de-seguridad-Duran.jpg" alt="Cumbe contribuyendo a ordenanza de lote mínimo">
            <div class="card-content">
                <h3>Cumbe aportó a la construcción participativa del lote mínimo</h3>
                <p>Cumbe contribuye a la construcción participativa de la ordenanza del lote mínimo, promoviendo el desarrollo urbano sostenible.</p>
                <a href="https://mileniumtvi.com/cumbe-aporto-a-la-construccion-participativa-del-lote-minimo" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <img loading="lazy" src="https://mileniumtvi.com/wp-content/uploads/2025/07/Bloque-de-seguridad-Duran.jpg" alt="Cuenca reconocida como ciudad más segura de Sudamérica por Numbeo">
            <div class="card-content">
                <h3>Cuenca, ciudad más segura de Sudamérica según Numbeo</h3>
                <p>Cuenca ha sido reconocida como la ciudad más segura de Sudamérica por el índice Numbeo, destacando por sus bajos índices de criminalidad y la calidad de vida que ofrece a sus habitantes.</p>
                <a href="https://mileniumtvi.com/cuenca-ciudad-mas-segura-de-sudamerica-segun-numbeo" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <img loading="lazy" src="https://mileniumtvi.com/wp-content/uploads/2025/07/Bloque-de-seguridad-Duran.jpg" alt="Santa Ana incorporándose a ordenanza de lote mínimo">
            <div class="card-content">
                <h3>Santa Ana se suma a la construcción de la ordenanza del lote mínimo</h3>
                <p>La parroquia Santa Ana se incorpora al proceso de elaboración de la ordenanza sobre el lote mínimo, promoviendo el desarrollo urbano sostenible y regulando el uso del suelo en la región.</p>
                <a href="https://mileniumtvi.com/santa-ana-se-suma-a-la-construccion-de-la-ordenanza-del-lote-minimo" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <img loading="lazy" src="https://mileniumtvi.com/wp-content/uploads/2025/07/Bloque-de-seguridad-Duran.jpg" alt="Entrega de beneficios a juntas de agua en Pichincha">
            <div class="card-content">
                <h3>Entrega de beneficios a las juntas de agua potable y riego de Pichincha</h3>
                <p>Se realiza la entrega de beneficios a las juntas de agua potable y riego en Pichincha, mejorando el acceso al agua y apoyando la agricultura local mediante recursos y asistencia técnica.</p>
                <a href="https://mileniumtvi.com/entrega-de-beneficios-a-las-juntas-de-agua-potable-y-riego-de-pichincha" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <img loading="lazy" src="https://mileniumtvi.com/wp-content/uploads/2025/07/Bloque-de-seguridad-Duran.jpg" alt="Implementación de sistemas de agua y alcantarillado en Baba">
            <div class="card-content">
                <h3>Sistemas de Agua Potable y Alcantarillado para Baba</h3>
                <p>Se implementan nuevos sistemas de agua potable y alcantarillado pluvial en Baba para mejorar la calidad de vida y la infraestructura local.</p>
                <a href="https://mileniumtvi.com/sistemas-de-agua-potable-y-alcantarillado-pluvial-para-baba" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <img loading="lazy" src="https://mileniumtvi.com/wp-content/uploads//screen_shot_2025-07-30_at_10.09.33_am.png" alt="3er Festival de la Fritada en Sidcay con gastronomía y actividades">
            <div class="card-content">
                <h3>Sidcay se llenará de sabor con el 3er Festival de la Fritada</h3>
                <p>El 3er Festival de la Fritada en Sidcay promete deleitar a los asistentes con gastronomía, música y actividades culturales para toda la familia.</p>
                <a href="https://mileniumtvi.com/sidcay-se-llenara-de-sabor-con-el-3er-festival-de-la-fritada" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <img loading="lazy" src="https://mileniumtvi.com/wp-content/uploads/2025/07/Bloque-de-seguridad-Duran.jpg" alt="Convocatoria para certamen Reina de Cuenca 2025-2026">
            <div class="card-content">
                <h3>Certamen Reina de Cuenca</h3>
                <p>Cuenca se prepara para elegir a su Reina. El certamen se desarrollará el jueves 23 de octubre en el Teatro Carlos Cueva Tamariz, y las inscripciones estarán disponibles en la página oficial de Instagram: Fundación Reinas de Cuenca.</p>
                <a href="https://mileniumtvi.com/-convocan-al-certamen-reina-de-cuenca-2025-2026" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <img loading="lazy" src="https://img.youtube.com/vi/-a8ElTs6Pds/hqdefault.jpg" alt="Suspensión temporal de trabajos de bacheo en Cuenca">
            <div class="card-content">
                <h3>Noticia Local</h3>
                <p>La Dirección de Obras Públicas de Cuenca suspende temporalmente trabajos de bacheo y asfaltado por falta de materiales de la Refinería de Esmeraldas.</p>
                <a href="https://www.youtube.com/embed/-a8ElTs6Pds" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
    </div>
</section>


    <!-- Noticia en Imágenes -->
    <section id="imagenes" class="section">
        <h2>Noticia en Imágenes</h2>
        <div class="grid">
            <div class="card">
                <img loading="lazy" src="https://img.youtube.com/vi/2wOBH_5rgJQ/hqdefault.jpg" alt="Visita de Marco Rubio al Presidente Daniel Noboa en Carondelet">
                <div class="card-content">
                    <h3>Visita de Marco Rubio al Presidente Daniel Noboa en Carondelet</h3>
                    <p>Marco Rubio, Secretario de Estado de Estados Unidos, visitó al Presidente Daniel Noboa en Carondelet.</p>
                    <a href="https://youtu.be/2wOBH_5rgJQ?si=olw4C5W15LH7DtRL" target="_blank" rel="noopener noreferrer">Ver video</a>
                </div>
            </div>
            <div class="card">
                <img loading="lazy" src="https://img.youtube.com/vi/3Ws3KFTv4pE/hqdefault.jpg" alt="Evento de colocación de primera piedra para distribuidor de tráfico Monay - ÍESS">
                <div class="card-content">
                    <h3>Distribuidor de Tráfico Monay - ÍESS</h3>
                    <p>El presidente de la República, Daniel Noboa Azín, lideró el evento simbólico de colocación de la primera piedra de la construcción del distribuidor de tráfico Monay - ÍESS ubicada en Azuay.</p>
                    <a href="https://youtu.be/3Ws3KFTv4pE" target="_blank" rel="noopener noreferrer">Ver video</a>
                </div>
            </div>
            <div class="card">
                <img loading="lazy" src="https://img.youtube.com/vi/3Ws3KFTv4pE/hqdefault.jpg" alt="Inauguración de Central Termoeléctrica El Descanso II en Azogues">
                <div class="card-content">
                    <h3>Inauguración Central Termoeléctrica El Descanso II</h3>
                    <p>Este 30 de julio de 2025, el presidente de la República, Daniel Noboa Azin, inauguró la Central Termoeléctrica Terrestre El Descanso II, ubicada en el cantón Azogues, provincia del Cañar.</p>
                    <a href="https://youtu.be/z1xQfEvFjA8?si=deueu9QrihN2rcYY" target="_blank" rel="noopener noreferrer">Ver video</a>
                </div>
            </div>
            <div class="card">
                <img loading="lazy" src="https://img.youtube.com/vi/z77l-H4H664/hqdefault.jpg" alt="Accidente fatal en vía Cuenca - Girón - Pasaje">
                <div class="card-content">
                    <h3>Accidente en Cuenca - Girón - Pasaje</h3>
                    <p>2 personas fallecieron en un grave accidente de tránsito en la vía Cuenca - Girón - Pasaje este martes. Uno es un niño de 4 años de edad.</p>
                    <a href="https://youtu.be/z77l-H4H664?si=Ey-LekZGWl7tz1-D" target="_blank" rel="noopener noreferrer">Ver video</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Videos -->
    <section id="videos" class="section">
        <h2>Videos</h2>
        <div class="grid">
            <div class="card">
                <iframe loading="lazy" width="100%" height="315" src="https://www.youtube.com/embed/MHjAUKw1VAE" title="Video Viral de la semana" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                <div class="card-content">
                    <h3>Video Viral</h3>
                    <p>Mira los videos más populares de la semana.</p>
                </div>
            </div>
            <div class="card">
                <iframe loading="lazy" width="100%" height="315" src="https://www.youtube.com/embed/WIc2_BaF0Mo?si=GMguO6tXNOpN9GYc" title="Entrevista Exclusiva con celebridad" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
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
                <a href="https://mileniumtvi.com/mas-de-100-ciudadanos-de-perucho-se-certifican-en-herramientas-digitales-y-rompen-la-brecha-tecnologica" rel="noopener noreferrer">
                    <img loading="lazy" src="https://via.placeholder.com/250x150" alt="Certificación en herramientas digitales en Perucho">
                </a>
                <div class="card-content">
                    <h3>Transformación Digital en Perucho</h3>
                    <p>La parroquia rural de Perucho en Quito vivió este miércoles 30 de julio, una jornada de transformación digital.</p>
                    <a href="https://mileniumtvi.com/mas-de-100-ciudadanos-de-perucho-se-certifican-en-herramientas-digitales-y-rompen-la-brecha-tecnologica" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <a href="https://mileniumtvi.com/el-80--de-las-enfermedades-cronicas-se-pueden-prevenir-con-autocuidadopor-ciento-" rel="noopener noreferrer">
                <img loading="lazy" src="https://via.placeholder.com/250x150" alt="Prevención de enfermedades crónicas con autocuidado">
            </a>
            <div class="card-content">
                <h3>80% de enfermedades crónicas prevenibles con autocuidado</h3>
                <p>Expertos destacan que el 80% de las enfermedades crónicas pueden prevenirse con prácticas de autocuidado, promoviendo hábitos saludables.</p>
                <a href="https://mileniumtvi.com/el-80--de-las-enfermedades-cronicas-se-pueden-prevenir-con-autocuidadopor-ciento-" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <a href="https://mileniumtvi.com/jose-adolfo-fito-macias-villamar-lider-de-la-organizacion-criminal-transnacional-los-choneros-fue-extraditado" rel="noopener noreferrer">
                <img loading="lazy" src="https://via.placeholder.com/250x150" alt="Extradición de José Adolfo Fito Macías, líder de Los Choneros">
            </a>
            <div class="card-content">
                <h3>Extradición de Fito Macías</h3>
                <p>José Adolfo Fito Macías, líder de Los Choneros, fue extraditado, marcando un hito en la lucha contra el crimen organizado.</p>
                <a href="https://mileniumtvi.com/jose-adolfo-fito-macias-villamar-lider-de-la-organizacion-criminal-transnacional-los-choneros-fue-extraditado" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <a href="https://mileniumtvi.com/ecuador-y-emiratos-arabes-unidos-fortalecen-lazos-de-cooperacion" rel="noopener noreferrer">
                <img loading="lazy" src="https://via.placeholder.com/250x150" alt="Acuerdos entre Ecuador y Emiratos Árabes Unidos para turismo y seguridad">
            </a>
            <div class="card-content">
                <h3>Artículo Especial</h3>
                <p>Ecuador y Emiratos Árabes Unidos firman acuerdos para impulsar turismo, conectividad aérea y seguridad, promoviendo intercambios culturales.</p>
                <a href="https://mileniumtvi.com/ecuador-y-emiratos-arabes-unidos-fortalecen-lazos-de-cooperacion" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <a href="https://mileniumtvi.com/ecuador-y-emiratos-arabes-unidos-fortalecen-lazos-de-cooperacion" rel="noopener noreferrer">
                <img loading="lazy" src="https://via.placeholder.com/250x150" alt="Oportunidades comerciales entre Ecuador y Emiratos Árabes">
            </a>
            <div class="card-content">
                <h3>Blog del Mes</h3>
                <p>Descubre cómo los lazos entre Ecuador y Emiratos Árabes abren oportunidades para el comercio y la innovación tecnológica.</p>
                <a href="https://mileniumtvi.com/ecuador-y-emiratos-arabes-unidos-fortalecen-lazos-de-cooperacion" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <a href="https://mileniumtvi.com/ya-puedes-viajar-en-tren-por-la-ruta-nariz-del-diablo-de-ecuador" rel="noopener noreferrer">
                <img loading="lazy" src="https://via.placeholder.com/250x150" alt="Viaje en tren por Ruta Nariz del Diablo en Ecuador">
            </a>
            <div class="card-content">
                <h3>Ruta Nariz del Diablo</h3>
                <p>Ya está disponible el viaje en tren por la icónica Ruta Nariz del Diablo, ofreciendo una experiencia única en Ecuador.</p>
                <a href="https://mileniumtvi.com/ya-puedes-viajar-en-tren-por-la-ruta-nariz-del-diablo-de-ecuador" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
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
    // Smooth scroll para los enlaces de navegación
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function (e) {
            e.preventDefault();
            document.querySelector(this.getAttribute('href')).scrollIntoView({
                behavior: 'smooth'
            });
        });
    });

    // Año dinámico en footer
    document.getElementById('current-year').textContent = new Date().getFullYear();

    // Toggle menú hamburguesa
    document.querySelector('.menu-toggle').addEventListener('click', () => {
        document.querySelector('nav ul').classList.toggle('active');
    });
</script>
</body>
</html>

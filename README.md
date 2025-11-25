

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
            <!-- Canal 1: Milenium TVI Principal -->
            <div class="video-wrapper">
                <iframe 
                    src="https://app.viloud.tv/embed/channel/c8984eee3163b175a0c725860f53749d?autoplay=false&muted=false" 
                    width="100%" 
                    height="360" 
                    frameborder="0" 
                    allowfullscreen 
                    allow="autoplay; encrypted-media" 
                    title="Transmisión en vivo del canal principal de Milenium Tvi">
                </iframe>
            </div>
            <p>Transmisión en vivo del canal principal de Milenium Tvi.</p>

            <!-- Canal 2: MTVI2 Musical -->
            <div class="video-wrapper">
                <iframe 
                    src="https://app.viloud.tv/embed/channel/119c56a41cef4bf9b47e6d600cc70a63?autoplay=false&muted=false" 
                    width="100%" 
                    height="360" 
                    frameborder="0" 
                    allowfullscreen 
                    allow="autoplay; encrypted-media" 
                    title="MTVI2 Musical - Música en vivo">
                </iframe>
            </div>
            <p>Disfruta de la mejor selección de música en vivo con MTVI2 Musical.</p>

            <!-- Canal 3: MTVI3 Películas -->
            <div class="video-wrapper">
                <iframe 
                    src="https://app.viloud.tv/embed/channel/fa28724c715bb373296ca57a2dcd551c?autoplay=false&muted=false" 
                    width="100%" 
                    height="360" 
                    frameborder="0" 
                    allowfullscreen 
                    allow="autoplay; encrypted-media" 
                    title="MTVI3 Películas - Streaming continuo">
                </iframe>
            </div>
            <p>Las mejores películas en streaming continuo con MTVI3 Películas.</p>

            <!-- Canal 4: MTVI4 Series -->
            <div class="video-wrapper">
                <iframe 
                    src="https://app.viloud.tv/embed/channel/8823313f19b20ef55dea4f3ad8a4cab7?autoplay=false&muted=false" 
                    width="100%" 
                    height="360" 
                    frameborder="0" 
                    allowfullscreen 
                    allow="autoplay; encrypted-media" 
                    title="MTVI4 Series - Tus series favoritas en vivo">
                </iframe>
            </div>
            <p>Tus series favoritas en transmisión en vivo con MTVI4 Series.</p>
        </div>
    </section>






    <!-- TV Play -->
<section id="tvplay" class="section">
    <h2>TV Play</h2>
    <div class="grid">
       

        <!-- NUEVAS TARJETAS AL INICIO -->
        <div class="card">
            <iframe loading="lazy" width="100%" height="315" src="https://www.youtube.com/embed/krueypTySow?feature=share" title="Arte Circular en Cuenca 28,29 y 30 de noviembre" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            <div class="card-content">
                <h3>Arte Circular en Cuenca 28,29 y 30 de noviembre</h3>
                <p>Evento cultural de arte circular en Cuenca los días 28, 29 y 30 de noviembre.</p>
            </div>
        </div>
        <div class="card">
            <iframe loading="lazy" width="100%" height="315" src="https://www.youtube.com/embed/1qga_FKWYL0?feature=share" title="Remigio Hurtado Presidente de los Servidores Públicos" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            <div class="card-content">
                <h3>Remigio Hurtado Presidente de los Servidores Públicos</h3>
                <p>Entrevista o segmento con Remigio Hurtado, Presidente de los Servidores Públicos.</p>
            </div>
        </div>

        <!-- Contenido original (sin cambios) -->
        <div class="card">
            <iframe loading="lazy" width="100%" height="315" src="https://www.youtube.com/embed/brgDCi26lUQ?si=Hhr-ETQKVjf_nl5S" title="Expresión Popular con Diego Idrovo" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            <div class="card-content">
                <h3>Expresión Popular con Diego Idrovo</h3>
                <p>Diego Idrovo, Presidente de la Cámara de Transporte de Cuenca, analiza la tarifa del servicio urbano de buses en #ExpresionPopular</p>
            </div>
        </div>
        <div class="card">
            <iframe loading="lazy" width="100%" height="315" src="https://www.youtube.com/embed/UyqlRsYiNIM?si=mVWrFf56yBosP7fa" title="Consejos de Nutrición con la Dra. Rocío Medina" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            <div class="card-content">
                <h3>Consejos de Nutrición con la Dra. Rocío Medina</h3>
                <p>La Dra. Rocío Medina es Vicepresidenta e integrante del Consejo Consultor de Nutrición (NAB, por sus siglas en inglés) de Herbalife, donde contribuye con su experiencia médica y científica en el desarrollo de estrategias y productos orientados a la nutrición y el bienestar nos comparte consejos prácticos sobre cómo llevar una alimentación equilibrada a lo largo del día.</p>
            </div>
        </div>
        <div class="card">
            <iframe loading="lazy" width="100%" height="315" src="https://www.youtube.com/embed/nm3iahkSKwc?si=l7M2Bjy1pz-38Wbn" title="Conferencia Científica Orquideas Andinas" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            <div class="card-content">
                <h3>Conferencia Científica Orquideas Andinas</h3>
                <p>Juan Pablo Martínez científico de Ecuagénera entrega detalles de la Conferencia Científica Orquideas Andinas, evento que se organiza con Diners Club y la USFQ.</p>
            </div>
        </div>
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












   <!-- Noticias -->
<section id="news" class="section">
    <h2>Noticias</h2>
    <div class="grid">
        <div class="card">
            <div class="card-content">
                <h3>CELEC EP invierte en formación universitaria</h3>
                <p>La Corporación Eléctrica del Ecuador (CELEC EP) invierte en la formación universitaria de jóvenes de zonas hidroeléctricas, entregando becas completas para estudiar Ingeniería Ambiental y Energías Alternativas.</p>
                <a href="https://mileniumtvi.com/celec-ep-invierte-en-formacion-universitaria" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Carolina Haro es la nueva directora de SNGR</h3>
                <p>Carolina Lozano Haro inicia su gestión al frente de la Secretaría de Gestión de Riesgos con una agenda técnica y de articulación institucional.</p>
                <a href="https://mileniumtvi.com/carolina-haro-es-la-nueva-directora-de-sngr1" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>II Congreso de Cajas de Ahorro y Cajas Solidarias 2025</h3>
                <p>Más de 500 mujeres se reúnen en Cuenca en el II Congreso de Cajas de Ahorro y Cajas Solidarias 2025, promoviendo el empoderamiento financiero y solidario.</p>
                <a href="https://mileniumtvi.com/ii-congreso-de-cajas-de-ahorro-y-cajas-solidarias-2025" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Ecuador se consolida como exportador de lácteos</h3>
                <p>Ecuador se consolida como exportador de lácteos al enviar 2.503 toneladas en dos años, generando USD 6,2 millones en ingresos por exportaciones.</p>
                <a href="https://mileniumtvi.com/cuador-se-consolida-como-exportador-de-lacteos" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Vicepresidencia y UNICEF suscriben memorando</h3>
                <p>La Vicepresidencia y UNICEF suscriben un Memorando de Entendimiento para garantizar los derechos de la niñez en Ecuador mediante acciones conjuntas.</p>
                <a href="https://mileniumtvi.com/vicepresidencia-y-unicef-suscriben-memorando" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Oído y ACV</h3>
                <p>Se revela la conexión poco conocida entre problemas de oído y accidentes cerebrovasculares, destacando la importancia de la salud auditiva para prevenir riesgos vasculares.</p>
                <a href="https://mileniumtvi.com/oido-y-acv" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Se lanzó la Ronda Intercampos</h3>
                <p>Se lanzó la Ronda Intracampos III que captará más de USD 360 millones en inversiones para el beneficio del sector petrolero del país.</p>
                <a href="https://mileniumtvi.com/se-lanzo-la-ronda-intercamopos" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>La primera boletería solo para humanos llega de la mano de World y Mundo Arjona</h3>
                <p>Se introduce la primera boletería "solo para humanos" para eventos de World y Mundo Arjona, utilizando tecnología para prevenir la reventa por bots y garantizar acceso equitativo.</p>
                <a href="https://mileniumtvi.com/la-primera-boleteroa-solo-para-humanos-llega-de-la-mano-de-world-y-mundo-arjona" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Cañar se conecta</h3>
                <p>El Gobierno Nacional inaugura un Nuevo Punto Digital Gratuito en Azogues, conectando a la provincia de Cañar con oportunidades digitales y acceso a internet de calidad.</p>
                <a href="https://mileniumtvi.com/canar-se-conecta" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>El presidente Daniel Noboa dispone cambios en el gabinete ministerial</h3>
                <p>El presidente Daniel Noboa dispone cambios en el gabinete ministerial para fortalecer la administración pública y avanzar en las prioridades nacionales.</p>
                <a href="https://mileniumtvi.com/el-presidente-daniel-noboa-dispone-cambios-en-el-gabinete-ministerial" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Registro en el país SNGR</h3>
                <p>Ecuador inicia el Mapatón Anual Nacional 2025 para fortalecer la respuesta ante emergencias mediante el mapeo colaborativo de datos geográficos.</p>
                <a href="https://mileniumtvi.com/regsitro-en-el-pais-sngr" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Arte circular en Cuenca</h3>
                <p>Arte Circular regresa a Cuenca con esculturas hechas de neumáticos reciclados por segundo año consecutivo, ofreciendo entrada gratuita y promoviendo la sostenibilidad.</p>
                <a href="https://mileniumtvi.com/arte-circular-en-cuenca" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Caminos de luz para iluminar escuelas</h3>
                <p>El Gobierno impulsa el programa "Caminos de Luz" para instalar iluminación en escuelas rurales, mejorando la seguridad y el acceso educativo.</p>
                <a href="https://mileniumtvi.com/-caminos-de-luz-para-iluminar-escuelas" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Ecuador y Colombia culminan proyecto</h3>
                <p>La cooperación binacional entre Ecuador y Colombia logra el 100% de metas en el proyecto de gobernanza hídrica compartida, fortaleciendo la gestión de recursos hídricos transfronterizos.</p>
                <a href="https://mileniumtvi.com/ecuador-y-colombia-culminan-proyecto" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Por la salud mental</h3>
                <p>Ecuador firma el histórico Pacto Nacional por la Salud Mental para promover políticas integrales que aborden el bienestar psicológico de la población.</p>
                <a href="https://mileniumtvi.com/por-la-salud-mental" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Foro Nacional Urbano 2025</h3>
                <p>El Gobierno impulsa “Ciudades del Futuro” en el Foro Urbano Nacional 2025 en Cuenca, promoviendo un Ecuador sostenible mediante planificación urbana innovadora.</p>
                <a href="https://mileniumtvi.com/foro-nacional-urbano-2025" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <div class="card-content">
                <h3>Los puntos digitales gratuitos se proyectan como semilleros de innovación para emprendedores</h3>
                <p>Los Puntos Digitales Gratuitos se posicionan como espacios clave para fomentar la innovación y el emprendimiento mediante acceso a herramientas tecnológicas y capacitación.</p>
                <a href="https://mileniumtvi.com/los-puntos-digitales-gratuitos-se-proyectan-como-semilleros-de-innovacion-para-emprendedores-" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
    </div>
</section>





    html

<!-- Noticias Locales -->
<section id="locales" class="section">
    <h2>Noticias Locales</h2>
    <div class="grid">

        <!-- NUEVAS NOTICIAS AL INICIO -->
        <div class="card">
            <a href="https://youtu.be/XsS51vDleGI" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/XsS51vDleGI/hqdefault.jpg" alt="3 PPLs se fugaron del CLP Azogues">
            </a>
            <div class="card-content">
                <h3>3 PPLs se fugaron del CLP Azogues, uno fue recapturado</h3>
                <p>3 PPLs se fugaron del CLP Azogues, uno fue recapturado. La madrugada de este miércoles 163 reos fueron trasladados desde Azogues hasta Turi. Funcionarios del SNAI se encuentran aprehendidos y puestos a órdenes de la fiscalía por el delito de Evasión.</p>
                <a href="https://youtu.be/XsS51vDleGI" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>

        <div class="card">
            <a href="https://youtu.be/I9eZ3wBCmb4" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/I9eZ3wBCmb4/hqdefault.jpg" alt="Un rayo arrancó la cabeza del monumento a Cristo Rey de Cullca">
            </a>
            <div class="card-content">
                <h3>Un rayo arrancó la cabeza del monumento a Cristo Rey de Cullca</h3>
                <p>Un rayo cercenó la cabeza del monumento a Cristo Rey de Cullca la tarde de este martes. Este monumento tiene una antigüedad de más de 90 años.</p>
                <a href="https://youtu.be/I9eZ3wBCmb4" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>

        <div class="card">
            <a href="https://youtu.be/6K8Iz6diL5s" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/6K8Iz6diL5s/hqdefault.jpg" alt="Obras en el Estadio Alejandro Serrano Aguilar">
            </a>
            <div class="card-content">
                <h3>Obras en el Estadio Alejandro Serrano Aguilar registra un 60% de avance</h3>
                <p>La readecuación del Estadio Alejandro Serrano Aguilar registra un 60% de avance.</p>
                <a href="https://youtu.be/6K8Iz6diL5s" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>

        <div class="card">
            <a href="https://youtu.be/Kc1Gh7hB4Jo" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/Kc1Gh7hB4Jo/hqdefault.jpg" alt="Vicepresidencia y UNFPA firman alianza histórica">
            </a>
            <div class="card-content">
                <h3>Vicepresidencia y UNFPA firman alianza histórica contra el embarazo adolescente</h3>
                <p>Vicepresidencia y UNFPA firman alianza histórica contra el embarazo adolescente. Memorando de Entendimiento fortalecerá la Política Intersectorial 2026-2035 con estándares internacionales y modelos basados en evidencia.</p>
                <a href="https://youtu.be/Kc1Gh7hB4Jo" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>

        <div class="card">
            <a href="https://youtu.be/tbDukyFxAFQ" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/tbDukyFxAFQ/hqdefault.jpg" alt="Portales de Seguridad Azuay-Guayas">
            </a>
            <div class="card-content">
                <h3>Los prefectos de Azuay y Guayas inauguran los Portales de Seguridad</h3>
                <p>Los prefectos de Azuay y Guayas inauguran los Portales de Seguridad para identificación facial y lector de placa de vehículos.</p>
                <a href="https://youtu.be/tbDukyFxAFQ" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>

        <div class="card">
            <a href="https://youtu.be/ra_T7Qnb3Kg" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/ra_T7Qnb3Kg/hqdefault.jpg" alt="Noboa logra nuevo acuerdo comercial agropecuario con Perú">
            </a>
            <div class="card-content">
                <h3>Noboa logra nuevo acuerdo comercial agropecuario con Perú</h3>
                <p>El Gobierno del Presidente Daniel Noboa logra nuevo acuerdo comercial agropecuario con Perú.</p>
                <a href="https://youtu.be/ra_T7Qnb3Kg" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>

        <!-- NOTICIAS ORIGINALES (se mantienen todas menos las últimas 5 eliminadas) -->
        <div class="card">
            <a href="https://youtu.be/dj78uPaSnEQ" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/dj78uPaSnEQ/hqdefault.jpg" alt="Vista previa de la noticia">
            </a>
            <div class="card-content">
                <h3>Noticia Local Reciente 1</h3>
                <p>Resumen breve de la noticia local presentada en el video.</p>
                <a href="https://youtu.be/dj78uPaSnEQ" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/YroEqqOjMvg" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/YroEqqOjMvg/hqdefault.jpg" alt="Vista previa de la noticia">
            </a>
            <div class="card-content">
                <h3>Noticia Local Reciente 2</h3>
                <p>Resumen breve de la noticia local presentada en el video.</p>
                <a href="https://youtu.be/YroEqqOjMvg" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/9mtM32IBoTw" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/9mtM32IBoTw/hqdefault.jpg" alt="Vista previa de la noticia">
            </a>
            <div class="card-content">
                <h3>Noticia Local Reciente 3</h3>
                <p>Resumen breve de la noticia local presentada en el video.</p>
                <a href="https://youtu.be/9mtM32IBoTw" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/oLjICggR4qg" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/oLjICggR4qg/hqdefault.jpg" alt="Vista previa de la noticia">
            </a>
            <div class="card-content">
                <h3>Noticia Local Reciente 4</h3>
                <p>Resumen breve de la noticia local presentada en el video.</p>
                <a href="https://youtu.be/oLjICggR4qg" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/NXmnYQwuoNk" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/NXmnYQwuoNk/hqdefault.jpg" alt="Vista previa de la noticia">
            </a>
            <div class="card-content">
                <h3>Noticia Local Reciente 5</h3>
                <p>Resumen breve de la noticia local presentada en el video.</p>
                <a href="https://youtu.be/NXmnYQwuoNk" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/KaCZjrs-Di8" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/KaCZjrs-Di8/hqdefault.jpg" alt="Vista previa de la noticia">
            </a>
            <div class="card-content">
                <h3>Noticia Local Reciente 6</h3>
                <p>Resumen breve de la noticia local presentada en el video.</p>
                <a href="https://youtu.be/KaCZjrs-Di8" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/Wdnkv98EwA8" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/Wdnkv98EwA8/hqdefault.jpg" alt="Vista previa de la noticia">
            </a>
            <div class="card-content">
                <h3>Noticia Local Reciente 7</h3>
                <p>Resumen breve de la noticia local presentada en el video.</p>
                <a href="https://youtu.be/Wdnkv98EwA8" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/pDkzEFxwOaI?si=Fds_bUKw-yx974k_" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/pDkzEFxwOaI/hqdefault.jpg" alt="Muerte de 4 PPL´s en centro de rehabilitación de Turi">
            </a>
            <div class="card-content">
                <h3>Muerte de 4 PPL´s en centro de rehabilitación de Turi</h3>
                <p>El sábado 1 de noviembre la policía reportó la muerte de 4 PPL´s en el centro de rehabilitación de Turi, en el pabellón de máxima seguridad.</p>
                <a href="https://youtu.be/pDkzEFxwOaI?si=Fds_bUKw-yx974k_" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/2q_bKAhVioM?si=WhK_mxtlOfpPX_De" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/2q_bKAhVioM/hqdefault.jpg" alt="Presidente Noboa en feria CIDAP">
            </a>
            <div class="card-content">
                <h3>Presidente Noboa recorre feria CIDAP y condecora a artesanos</h3>
                <p>El presidente de la República Daniel Noboa recorrió la feria del Centro Interamericano de Artes Populares CIDAP en el marco de las fiestas de independencia de #Cuenca.. El mandatario condecoró a dos artesanos del país: un joyero y una ceramista, por su trayectoria y su aporte para el desarrollo del país. El mandatario llegó con su esposa y su pequeño hijo Alvarito. En la feria participan 180 artesanos.</p>
                <a href="https://youtu.be/2q_bKAhVioM?si=WhK_mxtlOfpPX_De" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/V3M8tVy9C1c?si=PgbBbr9GQDdTtN-i" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/V3M8tVy9C1c/hqdefault.jpg" alt="Resoluciones del Consejo de Seguridad">
            </a>
            <div class="card-content">
                <h3>Resoluciones del Consejo de Seguridad</h3>
                <p>El Alcalde Cristian Zamora anuncia las resoluciones tomadas por el Consejo de Seguridad reunido este miércoles</p>
                <a href="https://youtu.be/V3M8tVy9C1c?si=PgbBbr9GQDdTtN-i" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/keBwRYjVtOs?si=x9xUTttN4hb8hkOm" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/keBwRYjVtOs/hqdefault.jpg" alt="Ataque armado en Barrial Blanco">
            </a>
            <div class="card-content">
                <h3>Ataque armado en Barrial Blanco</h3>
                <p>Un nuevo ataque armado se registró la noche de éste miércoles en el sector de la terminal terrestre Barrial Blanco en Cuenca</p>
                <a href="https://youtu.be/keBwRYjVtOs?si=x9xUTttN4hb8hkOm" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/BBiGUAU4Wi0?si=iqlQs5UjyqSgL09-" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/BBiGUAU4Wi0/hqdefault.jpg" alt="Conato de incendio en Nutri Leche">
            </a>
            <div class="card-content">
                <h3>Conato de incendio en Nutri Leche</h3>
                <p>Conato de incendio la tarde de este lunes en la planta de Nutri Leche del Parque industrial de Cuenca</p>
                <a href="https://youtu.be/BBiGUAU4Wi0?si=iqlQs5UjyqSgL09-" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/9Z6BkOa_svU?si=RBM-nf7Hs4nrphjH" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/9Z6BkOa_svU/hqdefault.jpg" alt="Carlos Morales sobre minería en Río Blanco">
            </a>
            <div class="card-content">
                <h3>Carlos Morales sobre minería en Río Blanco</h3>
                <p>Carlos Morales Presidente del GAD Parroquial de Molleturo rechaza versiones de que en el proyecto minero Río Blanco exista minería ilegal como lo aseguro días atrás el ejército...</p>
                <a href="https://youtu.be/9Z6BkOa_svU?si=RBM-nf7Hs4nrphjH" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/_BKyxsWS6fg?si=G-RO6xTx7CXoUElD" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/_BKyxsWS6fg/hqdefault.jpg" alt="Mini Cholita Cuencana 2025">
            </a>
            <div class="card-content">
                <h3>Mini Cholita Cuencana 2025</h3>
                <p>Amelia Paulina Bernal representante de la parroquia Ricaurte es la mini Cholita Cuencana 2025</p>
                <a href="https://youtu.be/_BKyxsWS6fg?si=G-RO6xTx7CXoUElD" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/nvlommafHrA?si=lwf9Y-cNiVMs37F8" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/nvlommafHrA/hqdefault.jpg" alt="Entrega de USD 6,9 millones en Azuay">
            </a>
            <div class="card-content">
                <h3>Entrega de USD 6,9 millones en Azuay</h3>
                <p>Este miércoles 29 de octubre, el presidente de la República, Daniel Noboa Azin, entregó USD 6,9 millones a la ciudadanía a través de BanEcuador y la Corporación Nacional de Finanzas Populares y Solidarias (Conafips) en Azuay</p>
                <a href="https://youtu.be/nvlommafHrA?si=lwf9Y-cNiVMs37F8" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/7ODJW3NezA4?si=Y1eL3bHM5QtlkbrU" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/7ODJW3NezA4/hqdefault.jpg" alt="Segunda fase de Jóvenes en Acción">
            </a>
            <div class="card-content">
                <h3>Segunda fase de Jóvenes en Acción</h3>
                <p>El presidente de la República, Daniel Noboa Azín, inauguró oficialmente la segunda fase del programa, “Jóvenes en Acción”. En esta edición, cerca de 80.000 jóvenes desde octubre se han incorporado a diferentes áreas de los ministerios</p>
                <a href="https://youtu.be/7ODJW3NezA4?si=Y1eL3bHM5QtlkbrU" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://youtu.be/QXFklrLVWXo?si=RlIEIKUGSDxbkPP7" rel="noopener noreferrer">
                <img loading="lazy" src="https://img.youtube.com/vi/QXFklrLVWXo/hqdefault.jpg" alt="Embanderamiento en Parque Calderón">
            </a>
            <div class="card-content">
                <h3>Embanderamiento en Parque Calderón</h3>
                <p>El hemiciclo del Parque Calderón fue el escenario para el acto de embanderamiento de la ciudad, en honor a los 205 años de independencia de Santa Ana de los Ríos de Cuenca...</p>
                <a href="https://youtu.be/QXFklrLVWXo?si=RlIEIKUGSDxbkPP7" target="_blank" rel="noopener noreferrer">Ver video</a>
            </div>
        </div>
        <div class="card">
            <a href="https://mileniumtvi.com/n-una-noche-llena-de-emoci-n-elegancia-y-orgullo-cuencano-fue-elegida-martina-guzm-n-vega-como-reina-de-cuenca-2025-2026" rel="noopener noreferrer">
                <img loading="lazy" src="https://via.placeholder.com/250x150" alt="Martina Guzmán Vega elegida Reina de Cuenca 2025-2026">
            </a>
            <div class="card-content">
                <h3>¡Una noche llena de emoción, elegancia y orgullo cuencano! Fue elegida Martina Guzmán Vega como Reina de Cuenca 2025-2026</h3>
                <p>En un evento lleno de glamour y tradición, Martina Guzmán Vega fue coronada como Reina de Cuenca 2025-2026, representando la belleza, el talento y el orgullo de la ciudad.</p>
                <a href="https://mileniumtvi.com/n-una-noche-llena-de-emoci-n-elegancia-y-orgullo-cuencano-fue-elegida-martina-guzm-n-vega-como-reina-de-cuenca-2025-2026" target="_blank" rel="noopener noreferrer">Leer más</a>
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

<!-- Publicaciones -->
<section id="posts" class="section">
    <h2>Publicaciones</h2>
    <div class="grid">
        <div class="card">
            <a href="https://mileniumtvi.com/los-bots-y-los-deepfakes-impulsan-una-nueva-ola-de-fraude-cibernetico" rel="noopener noreferrer">
                <img loading="lazy" src="https://via.placeholder.com/250x150" alt="Los bots y los deepfakes impulsan una nueva ola de fraude cibernético">
            </a>
            <div class="card-content">
                <h3>Los bots y los deepfakes</h3>
                <p>Un análisis sobre cómo los bots y los deepfakes están transformando el panorama del fraude cibernético, generando nuevos desafíos para la seguridad digital.</p>
                <a href="https://mileniumtvi.com/los-bots-y-los-deepfakes-impulsan-una-nueva-ola-de-fraude-cibernetico" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
        <div class="card">
            <a href="https://mileniumtvi.com/paro-violencia-y-consulta" rel="noopener noreferrer">
                <img loading="lazy" src="https://via.placeholder.com/250x150" alt="Artículo de opinión sobre paro, violencia y consulta">
            </a>
            <div class="card-content">
                <h3>Paro, Violencia y Consulta</h3>
                <p>Un análisis profundo sobre los recientes paros, la violencia y la consulta popular, abordando sus implicaciones sociales y políticas en Ecuador.</p>
                <a href="https://mileniumtvi.com/paro-violencia-y-consulta" target="_blank" rel="noopener noreferrer">Leer más</a>
            </div>
        </div>
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













































</section><!-- Defensa del Televidente -->
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


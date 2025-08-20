<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Página oficial del canal de TV con transmisiones en vivo, noticias, videos y más.">
    <title>Canal de TV - Inicio</title>
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
            width: 100vw; /* Fondo ocupa el ancho completo de la pantalla */
        }

        .header-container {
            max-width: 1400px; /* Ampliado para más espacio */
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo img {
            height: 50px;
        }

        nav ul {
            list-style: none;
            display: flex;
            gap: 1rem; /* Reducido para evitar desbordamiento */
            align-items: center;
            flex-wrap: nowrap; /* Una sola fila */
            overflow-x: auto; /* Desplazamiento horizontal en móviles */
            white-space: nowrap;
            padding: 0.5rem 0;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s;
            font-size: 0.95rem; /* Tamaño ajustado */
            padding: 0.5rem;
        }

        nav ul li a:hover {
            color: #ffd700;
        }

        /* Hero Section */
        .hero {
            background: url('https://via.placeholder.com/1920x600') no-repeat center/cover;
            height: 500px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
        }

        .hero h1 {
            font-size: 2.5rem; /* Reducido para mejor legibilidad en móviles */
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
            padding: 2rem 1rem; /* Reducido para móviles */
            max-width: 1400px;
            margin: 0 auto;
        }

        .section h2 {
            font-size: 1.8rem; /* Ajustado */
            margin-bottom: 1.2rem;
            color: #ffd700;
        }

        #live h2 {
            color: #1a73e8;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); /* Ajustado para móviles */
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
            height: 140px; /* Ajustado */
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

            nav ul {
                gap: 0.5rem;
                padding: 0.5rem;
            }

            nav ul li a {
                font-size: 0.85rem;
                padding: 0.4rem;
            }

            .live-stream .video-js {
                height: 200px; /* Ajustado para móviles */
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
                grid-template-columns: 1fr; /* Una columna en pantallas muy pequeñas */
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="header-container">
            <nav>
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
    <section class="hero">
        <div>
            <h1>Bienvenidos a Milenium Tvi</h1>
            <p>Tu fuente de entretenimiento, noticias y mucho más</p>
            <button onclick="window.location.href='#live'">Ver Ahora</button>
        </div>
    </section>

    <!-- Transmisiones en Vivo -->
    <section id="live" class="section live-stream">
        <h2>Transmisiones en Vivo</h2>
        <div class="entrevistas-container">
            <div class="video-wrapper">
                <video
                    id="live-stream-player-1"
                    class="video-js vjs-default-skin"
                    controls
                    preload="auto"
                    width="100%"
                    height="100%"
                    data-setup='{}'>
                    <source src="https://app.viloud.tv/hls/channel/c8984eee3163b175a0c725860f53749d.m3u8" type="application/x-mpegURL">
                    <p class="vjs-no-js">
                        Para ver este video, habilita JavaScript y considera actualizar a un navegador que soporte video HTML5.
                    </p>
                </video>
            </div>
            <p>Transmisión en vivo del canal principal de Milenium Tvi.</p>
            <div class="video-wrapper">
                <video
                    id="live-stream-player-2"
                    class="video-js vjs-default-skin"
                    controls
                    preload="auto"
                    width="100%"
                    height="100%"
                    data-setup='{}'>
                    <source src="https://571561.gvideo.io/cmaf/571561_2798196/master.m3u8" type="application/x-mpegURL">
                    <p class="vjs-no-js">
                        Para ver este video, habilita JavaScript y considera actualizar a un navegador que soporte video HTML5.
                    </p>
                </video>
            </div>
            <p>Disfruta de la mejor selección de música en vivo con MTVI2 Musical.</p>
            <div class="video-wrapper">
                <video
                    id="live-stream-player-3"
                    class="video-js vjs-default-skin"
                    controls
                    preload="auto"
                    width="100%"
                    height="100%"
                    data-setup='{}'>
                    <source src="https://app.viloud.tv/hls/channel/fa28724c715bb373296ca57a2dcd551c.m3u8" type="application/x-mpegURL">
                    <p class="vjs-no-js">
                        Para ver este video, habilita JavaScript y considera actualizar a un navegador que soporte video HTML5.
                    </p>
                </video>
            </div>
            <p>Las mejores películas en streaming continuo con MTVI3 Películas.</p>
            <div class="video-wrapper">
                <video
                    id="live-stream-player-4"
                    class="video-js vjs-default-skin"
                    controls
                    preload="auto"
                    width="100%"
                    height="100%"
                    data-setup='{}'>
                    <source src="https://app.viloud.tv/hls/channel/8823313f19b20ef55dea4f3ad8a4cab7.m3u8" type="application/x-mpegURL">
                    <p class="vjs-no-js">
                        Para ver este video, habilita JavaScript y considera actualizar a un navegador que soporte video HTML5.
                    </p>
                </video>
            </div>
            <p>Tus series favoritas en transmisión en vivo con MTVI4 Series.</p>
        </div>
    </section>

    <!-- Entrevistas -->
    <section id="entrevistas" class="section live-stream">
        <h2>Entrevistas</h2>
        <div class="entrevistas-container">
            <div class="video-wrapper">
                <iframe
                    src="https://www.youtube.com/embed/XgmQAEQdTFI"
                    title="Análisis de la Situación de las Instituciones Financieras"
                    frameborder="0"
                    allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                    allowfullscreen>
                </iframe>
            </div>
            <p>Un análisis de la Situación de las Instituciones financieras del país con el analista: Ing. Hernán Bravo</p>
            <div class="video-wrapper">
                <iframe
                    src="https://www.youtube.com/embed/t6AcnjKj4xo"
                    title="Suspensión de operaciones de la Cooperativa CREA Ltda."
                    frameborder="0"
                    allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                    allowfullscreen>
                </iframe>
            </div>
            <p>La SEPS dispone la suspensión de operaciones y liquidación forzosa de la Cooperativa CREA Ltda. y garantiza la protección de los depósitos de los socios.</p>
            <div class="video-wrapper">
                <iframe
                    src="https://www.youtube.com/embed/pOYq1aaJHRk?si=B2nBmp5UC2dI_p0I"
                    title="Entrevista al Presidente de Ecuador Daniel Noboa Azín"
                    frameborder="0"
                    allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                    allowfullscreen>
                </iframe>
            </div>
            <p>Entrevista al Presidente de Ecuador Daniel Noboa Azín</p>
            <div class="video-wrapper">
                <iframe
                    src="https://www.youtube.com/embed/JReQmALQX4g?si=hhV0Z35AOG7uGafi"
                    title="Entrevista Exclusiva"
                    frameborder="0"
                    allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                    allowfullscreen>
                </iframe>
            </div>
            <p>El analista Hernán Bravo Ordóñez experto en Economía y Finanzas se pregunta: ¿Habrá más apagones en Ecuador? Un interesante análisis.</p>
        </div>
    </section>

    <!-- TV Play -->
    <section id="tvplay" class="section">
        <h2>TV Play</h2>
        <div class="grid">
            <div class="card">
                <iframe width="100%" height="315" src="https://www.youtube.com/embed/xc4BXbdbPgk" title="Programa Estelar" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" autoplay="false" allowfullscreen></iframe>
                <div class="card-content">
                    <h3>Programa Estelar</h3>
                    <p>Disfruta de nuestro programa insignia con invitados especiales.</p>
                </div>
            </div>
            <div class="card">
                <iframe width="100%" height="315" src="https://www.youtube.com/embed/QRV5teEvBlY" title="Serie Exclusiva" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" autoplay="false" allowfullscreen></iframe>
                <div class="card-content">
                    <h3>Serie Exclusiva</h3>
                    <p>Una serie que no te puedes perder, disponible en TV Play.</p>
                </div>
            </div>
            <div class="card">
                <iframe width="100%" height="315" src="https://app.viloud.tv/watch/video/21edc30065853fe936367b19712782ca" title="Noticiero de Ecuador TV" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" autoplay="false" allowfullscreen></iframe>
                <div class="card-content">
                    <h3>Noticiero de Ecuador TV</h3>
                    <p>Noticiero de Ecuador TV 31 de julio de 2025.</p>
                </div>
            </div>
            <div class="card">
                <iframe width="100%" height="315" src="https://app.viloud.tv/watch/video/5d804afd7690880df7c104d12e735c18" title="Reporte Especial" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" autoplay="false" allowfullscreen></iframe>
                <div class="card-content">
                    <h3>Reporte Especial</h3>
                    <p>Un análisis profundo de los eventos más relevantes del momento, con entrevistas y reportajes exclusivos.</p>
                </div>
            </div>
            <div class="card">
                <iframe width="100%" height="315" src="https://app.viloud.tv/watch/video/ace1f14d19a324c1c673e3cd9498b081" title="Noticiero DW" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" autoplay="false" allowfullscreen></iframe>
                <div class="card-content">
                    <h3>Noticiero DW</h3>
                    <p>DW Noticias 15 de agosto 2025.</p>
                </div>
            </div>
            <div class="card">
                <iframe width="100%" height="315" src="https://app.viloud.tv/watch/video/08fd90b3560b564a093c14838fb1169f" title="Telediario" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" autoplay="false" allowfullscreen></iframe>
                <div class="card-content">
                    <h3>Telediario</h3>
                    <p>Noticias 15 de agosto 2025.</p>
                </div>
            </div>
            <div class="card">
                <iframe width="100%" height="315" src="https://app.viloud.tv/watch/video/555265dbcfc35802b9183246e425b1d2" title="Especial: Cultura Ecuatoriana" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" autoplay="false" allowfullscreen></iframe>
                <div class="card-content">
                    <h3>Especial: Cultura Ecuatoriana</h3>
                    <p>Un recorrido por las tradiciones, gastronomía y arte que definen la riqueza cultural de Ecuador.</p>
                </div>
            </div>
            <div class="card">
                <iframe width="100%" height="315" src="https://app.viloud.tv/watch/video/6f2793f43bdeadfa7c6923474ca4ec61" title="Especial: Innovación en Ecuador" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" autoplay="false" allowfullscreen></iframe>
                <div class="card-content">
                    <h3>Especial: Innovación en Ecuador</h3>
                    <p>Descubre los avances tecnológicos y proyectos innovadores que están transformando el futuro de Ecuador.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Noticias -->
    <section id="news" class="section">
        <h2>Noticias</h2>
        <div class="grid">
            <div class="card">
                <img src="https://via.placeholder.com/250x150" alt="Mi Tienda del Nuevo Ecuador">
                <div class="card-content">
                    <h3>Mi Tienda del Nuevo Ecuador</h3>
                    <p>El programa "Mi Tienda del Nuevo Ecuador" impulsa el emprendimiento y el comercio local, apoyando a pequeños negocios con recursos y capacitación para su crecimiento.</p>
                    <a href="https://mileniumtvi.com/mi-tienda-del-nuevo-ecuador" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://via.placeholder.com/250x150" alt="600 mujeres recibirán becas educativas">
                <div class="card-content">
                    <h3>600 Mujeres Recibirán Becas Educativas</h3>
                    <p>El gobierno ecuatoriano otorgará becas educativas a 600 mujeres, promoviendo la igualdad de género y el acceso a la educación para fortalecer su desarrollo profesional.</p>
                    <a href="https://mileniumtvi.com/600-mujeres-recibiran-becas-educativas" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://via.placeholder.com/250x150" alt="Cooperación en seguridad entre Ecuador y Uruguay">
                <div class="card-content">
                    <h3>En Montevideo, los Presidentes de Ecuador y Uruguay Fortalecen Cooperación en Materia de Seguridad</h3>
                    <p>En Montevideo, los presidentes de Ecuador y Uruguay firman acuerdos para fortalecer la cooperación en seguridad, enfocándose en la lucha contra el crimen organizado y el narcotráfico.</p>
                    <a href="https://mileniumtvi.com/en-montevideo-los-presidentes-de-ecuador-y-uruguay-fortalecen-cooperacion-en-materia-de-seguridad-" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://via.placeholder.com/250x150" alt="Agenda oficial de Daniel Noboa en Argentina">
                <div class="card-content">
                    <h3>El Presidente Daniel Noboa Inició su Agenda Oficial en Argentina con Encuentros con Empresarios</h3>
                    <p>El presidente Daniel Noboa comenzó su visita oficial en Argentina con reuniones clave con empresarios, buscando atraer inversiones y fortalecer lazos comerciales.</p>
                    <a href="https://mileniumtvi.com/el-presidente-daniel-noboa-inicio-su-agenda-oficial-en-argentina-con-encuentros-con-empresarios" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://via.placeholder.com/250x150" alt="Obras viales en la carretera E487">
                <div class="card-content">
                    <h3>El presidente Noboa dio inicio a obras viales en la carretera E487</h3>
                    <p>El presidente Daniel Noboa dio inicio a las obras viales en la carretera E487, un proyecto clave para mejorar la conectividad y el desarrollo económico en las regiones afectadas.</p>
                    <a href="https://mileniumtvi.com/el-presidente-noboa-dio-inicio-a-obras-viales-en-la-carretera-e487" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://via.placeholder.com/250x150" alt="Proyectos agrícolas, comercio y turismo comunitario">
                <div class="card-content">
                    <h3>El gobierno de Daniel Noboa impulsa el desarrollo de proyectos agrícolas, de comercio y turismo comunitario</h3>
                    <p>El gobierno de Daniel Noboa promueve iniciativas para fortalecer la agricultura, el comercio y el turismo comunitario, con proyectos que buscan generar empleo y desarrollo sostenible en comunidades locales.</p>
                    <a href="https://mileniumtvi.com/el-gobierno-de-daniel-noboa-impulsa-el-desarrollo-de-proyectos-agricolas-de-comercio-y-turismo-comunitario-" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://via.placeholder.com/250x150" alt="Visitas oficiales de Noboa">
                <div class="card-content">
                    <h3>El presidente Noboa desarrollará visitas oficiales a Brasil, Uruguay, Argentina y Japón</h3>
                    <p>El presidente Daniel Noboa realizará visitas oficiales en agosto a Brasil, Uruguay, Argentina y Japón para fortalecer la cooperación internacional.</p>
                    <a href="https://mileniumtvi.com/el-presidente-noboa-desarrollara-visitas-oficiales-a-brasil-uruguay-argentina-y-japon-este-agosto" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://via.placeholder.com/250x150" alt="Labor de cuidadores">
                <div class="card-content">
                    <h3>El presidente Noboa reconoció la labor de cuidadores</h3>
                    <p>El presidente Noboa destacó la importancia de quienes dedican su vida a cuidar a los más vulnerables del país, entregando reconocimientos y apoyo.</p>
                    <a href="https://mileniumtvi.com/el-presidente-noboa-reconocio-la-labor-de-quienes-dedican-su-vida-a-cuidar-a-los-mas-vulnerables-del-pais" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://via.placeholder.com/250x150" alt="Impulso a la agricultura">
                <div class="card-content">
                    <h3>Impulso a la agricultura y empleo rural</h3>
                    <p>El Gobierno Nacional impulsa la agricultura con la entrega de beneficios productivos y fomento de plazas laborales para la juventud rural.</p>
                    <a href="https://mileniumtvi.com/el-gobierno-nacional-impulsa-la-agricultura-con-la-entrega-de-beneficios-productivos-y-fomento-de-plazas-laborales-para-la-juventud-rural" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://via.placeholder.com/250x150" alt="Crédito internacional">
                <div class="card-content">
                    <h3>Crédito de USD 250 millones para Ecuador</h3>
                    <p>La confianza internacional en Ecuador se fortalece con la recepción de un crédito por USD 250 millones para proyectos de desarrollo.</p>
                    <a href="https://mileniumtvi.com/la-confianza-internacional-en-ecuador-se-fortalece-el-pais-recibio-un-credito-por-usd-250-millones" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://via.placeholder.com/250x150" alt="Fortalecimiento penitenciario">
                <div class="card-content">
                    <h3>Fortalecimiento del sistema penitenciario</h3>
                    <p>El presidente Noboa fortalece el sistema penitenciario con la entrega de más de 4000 chalecos de protección balística y uniformes para guías.</p>
                    <a href="https://mileniumtvi.com/el-presidente-noboa-fortalece-el-sistema-penitenciario-entrego-mas-de-4000-chalecos-de-proteccion-balistica-y-uniformes-para-guias" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://via.placeholder.com/250x150" alt="Consulta popular de Noboa">
                <div class="card-content">
                    <h3>Consulta popular planteada por el presidente Noboa</h3>
                    <p>La consulta popular planteada por el presidente Noboa tendría 7 preguntas y se realizaría el domingo 14 de diciembre.</p>
                    <a href="https://mileniumtvi.com/la-consulta-popular-planteada-por-el-presidente-noboa-tendria-7-preguntas-y-seria-el-domingo-14-de-diciembre" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://via.placeholder.com/250x150" alt="Ecuador y Royal Caribbean">
                <div class="card-content">
                    <h3>Ecuador y Royal Caribbean</h3>
                    <p>Ecuador fortalece el turismo con un acuerdo estratégico con Royal Caribbean para promover cruceros en la costa ecuatoriana.</p>
                    <a href="https://mileniumtvi.com/ecuador-y-royal-caribbean" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://via.placeholder.com/250x150" alt="Minería responsable en Ecuador">
                <div class="card-content">
                    <h3>Ecuador fortalece la minería responsable</h3>
                    <p>Ecuador impulsa la minería responsable con nuevas políticas que equilibran el desarrollo económico y la sostenibilidad ambiental.</p>
                    <a href="https://mileniumtvi.com/ecuador-fortalece-la-mineria-responsable" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://via.placeholder.com/250x150" alt="Atención a pacientes oncológicos">
                <div class="card-content">
                    <h3>El Gobierno Nacional garantiza la atención de pacientes oncológicos</h3>
                    <p>El Gobierno Nacional duplicó los pagos a Solca para garantizar la atención a pacientes oncológicos, al transferir USD 26,2 millones en lo que va de este año.</p>
                    <a href="https://mileniumtvi.com/el-gobierno-nacional-garantiza-la-atencion-de-pacientes-oncologicos-pago-a-solca-usd-26-millones-en-lo-que-va-del-anio" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://via.placeholder.com/250x150" alt="Celebración de la lactancia materna">
                <div class="card-content">
                    <h3>Ecuador camino hoy por el mejor alimento del mundo</h3>
                    <p>Más de 11 mil voces se unen en Ecuador para celebrar el poder de la lactancia materna.</p>
                    <a href="https://mileniumtvi.com/ecuador-camino-hoy-por-el-mejor-alimento-del-mundo" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://via.placeholder.com/250x150" alt="Centro Deportivo y Cultural en Bajo Alto">
                <div class="card-content">
                    <h3>El presidente Noboa inauguró el Centro Deportivo y Cultural en Bajo Alto</h3>
                    <p>El presidente Daniel Noboa inauguró un Centro Deportivo y Cultural en la comuna Bajo Alto, El Guabo, que ofrece espacios para actividades recreativas y culturales, fomentando la integración comunitaria y el desarrollo local.</p>
                    <a href="https://mileniumtvi.com/el-presidente-noboa-inauguro-el-centro-deportivo-y-cultural-en-la-comuna-bajo-alto-del-canton-el-guabo" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://via.placeholder.com/250x150" alt="Desarrollo agrícola en Azogues">
                <div class="card-content">
                    <h3>El presidente Noboa impulsa el desarrollo agrícola en Azogues</h3>
                    <p>En Azogues, el presidente Daniel Noboa entregó recursos y beneficios a productores agrícolas, promoviendo la modernización del sector y el aumento de la productividad, con un enfoque en la sostenibilidad.</p>
                    <a href="https://mileniumtvi.com/el-presidente-noboa-impulsa-el-desarrollo-agricola-en-azogues-con-la-entrega-de-nuevos-beneficios" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://via.placeholder.com/250x150" alt="Nuevo respaldo energético para Ecuador">
                <div class="card-content">
                    <h3>Nuevo respaldo energético para Ecuador</h3>
                    <p>El gobierno impulsa un plan estratégico para fortalecer el sector energético, asegurando un suministro eléctrico estable y sostenible mediante nuevas inversiones y proyectos de infraestructura energética.</p>
                    <a href="https://mileniumtvi.com/nuevo-respaldo-energetico-para-ecuador" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://via.placeholder.com/250x150" alt="Distribuidor de Tráfico Monay - ÍESS en Azuay">
                <div class="card-content">
                    <h3>El distribuidor de tráfico Monay - ÍESS en Azuay</h3>
                    <p>El presidente Daniel Noboa lideró la colocación de la primera piedra del distribuidor de tráfico Monay - ÍESS en Azuay, una obra que optimizará la movilidad y aliviará la congestión vehicular en la región.</p>
                    <a href="https://mileniumtvi.com/el-distribuidor-de-trafico-monay-iess-en-azuay" target="_blank">Leer más</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Noticias Locales -->
    <section id="locales" class="section">
        <h2>Noticias Locales</h2>
        <div class="grid">
            <div class="card">
                <a href="https://mileniumtvi.com/el-alcalde-de-latinoamerica">
                    <img src="https://via.placeholder.com/250x150" alt="El Alcalde de Latinoamérica">
                </a>
                <div class="card-content">
                    <h3>El Alcalde de Latinoamérica</h3>
                    <p>Un reconocimiento al liderazgo regional en la gestión municipal, destacando iniciativas que transforman comunidades en América Latina.</p>
                    <a href="https://mileniumtvi.com/el-alcalde-de-latinoamerica" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <a href="https://mileniumtvi.com/el-cacao-ecuatoriano-brilla-en-el-salon-del-chocolate-de-paris">
                    <img src="https://via.placeholder.com/250x150" alt="Cacao ecuatoriano en París">
                </a>
                <div class="card-content">
                    <h3>El cacao ecuatoriano brilla en el Salón del Chocolate de París</h3>
                    <p>El cacao ecuatoriano destacó en el Salón del Chocolate de París, recibiendo reconocimientos por su calidad y sostenibilidad, consolidando a Ecuador como líder en el mercado global.</p>
                    <a href="https://mileniumtvi.com/el-cacao-ecuatoriano-brilla-en-el-salon-del-chocolate-de-paris" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/Bloque-de-seguridad-Duran.jpg" alt="Cumbe aportó a la construcción participativa del lote mínimo">
                <div class="card-content">
                    <h3>Cumbe aportó a la construcción participativa del lote mínimo</h3>
                    <p>Cumbe contribuye a la construcción participativa de la ordenanza del lote mínimo, promoviendo el desarrollo urbano sostenible.</p>
                    <a href="https://mileniumtvi.com/cumbe-aporto-a-la-construccion-participativa-del-lote-minimo" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/Bloque-de-seguridad-Duran.jpg" alt="Cuenca, ciudad más segura de Sudamérica">
                <div class="card-content">
                    <h3>Cuenca, ciudad más segura de Sudamérica según Numbeo</h3>
                    <p>Cuenca ha sido reconocida como la ciudad más segura de Sudamérica por el índice Numbeo, destacando por sus bajos índices de criminalidad y la calidad de vida que ofrece a sus habitantes.</p>
                    <a href="https://mileniumtvi.com/cuenca-ciudad-mas-segura-de-sudamerica-segun-numbeo" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/Bloque-de-seguridad-Duran.jpg" alt="Santa Ana se suma a la ordenanza del lote mínimo">
                <div class="card-content">
                    <h3>Santa Ana se suma a la construcción de la ordenanza del lote mínimo</h3>
                    <p>La parroquia Santa Ana se incorpora al proceso de elaboración de la ordenanza sobre el lote mínimo, promoviendo el desarrollo urbano sostenible y regulando el uso del suelo en la región.</p>
                    <a href="https://mileniumtvi.com/santa-ana-se-suma-a-la-construccion-de-la-ordenanza-del-lote-minimo" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/Bloque-de-seguridad-Duran.jpg" alt="Entrega de beneficios a juntas de agua en Pichincha">
                <div class="card-content">
                    <h3>Entrega de beneficios a las juntas de agua potable y riego de Pichincha</h3>
                    <p>Se realiza la entrega de beneficios a las juntas de agua potable y riego en Pichincha, mejorando el acceso al agua y apoyando la agricultura local mediante recursos y asistencia técnica.</p>
                    <a href="https://mileniumtvi.com/entrega-de-beneficios-a-las-juntas-de-agua-potable-y-riego-de-pichincha" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/Bloque-de-seguridad-Duran.jpg" alt="Sistemas de Agua Potable y Alcantarillado para Baba">
                <div class="card-content">
                    <h3>Sistemas de Agua Potable y Alcantarillado para Baba</h3>
                    <p>Se implementan nuevos sistemas de agua potable y alcantarillado pluvial en Baba para mejorar la calidad de vida y la infraestructura local.</p>
                    <a href="https://mileniumtvi.com/sistemas-de-agua-potable-y-alcantarillado-pluvial-para-baba" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://mileniumtvi.com/wp-content/uploads//screen_shot_2025-07-30_at_10.09.33_am.png" alt="3er Festival de la Fritada en Sidcay">
                <div class="card-content">
                    <h3>Sidcay se llenará de sabor con el 3er Festival de la Fritada</h3>
                    <p>El 3er Festival de la Fritada en Sidcay promete deleitar a los asistentes con gastronomía, música y actividades culturales para toda la familia.</p>
                    <a href="https://mileniumtvi.com/sidcay-se-llenara-de-sabor-con-el-3er-festival-de-la-fritada" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/Bloque-de-seguridad-Duran.jpg" alt="Certamen Reina de Cuenca">
                <div class="card-content">
                    <h3>Certamen Reina de Cuenca</h3>
                    <p>Cuenca se prepara para elegir a su Reina. El certamen se desarrollará el jueves 23 de octubre en el Teatro Carlos Cueva Tamariz, y las inscripciones estarán disponibles en la página oficial de Instagram: Fundación Reinas de Cuenca.</p>
                    <a href="https://mileniumtvi.com/-convocan-al-certamen-reina-de-cuenca-2025-2026" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://img.youtube.com/vi/-a8ElTs6Pds/hqdefault.jpg" alt="Noticia Local">
                <div class="card-content">
                    <h3>Noticia Local</h3>
                    <p>La Dirección de Obras Públicas de Cuenca suspende temporalmente trabajos de bacheo y asfaltado por falta de materiales de la Refinería de Esmeraldas.</p>
                    <a href="https://www.youtube.com/embed/-a8ElTs6Pds" target="_blank">Ver video</a>
                </div>
            </div>
            <div class="card">
                <a href="https://mileniumtvi.com/cuenca-inspira-los-sentidos-en-el-festival-raices-2025">
                    <img src="https://via.placeholder.com/250x150" alt="Festival Raíces 2025">
                </a>
                <div class="card-content">
                    <h3>Cuenca Inspira los Sentidos en el Festival Raíces 2025</h3>
                    <p>El Festival Raíces 2025 en Cuenca promete una experiencia cultural única, con gastronomía, música, arte y tradiciones que celebran la riqueza cultural de la región.</p>
                    <a href="https://mileniumtvi.com/cuenca-inspira-los-sentidos-en-el-festival-raices-2025">Leer más</a>
                </div>
            </div>
            <div class="card">
                <a href="https://mileniumtvi.com/la-banda-britanica-oficial-de-tributo-a-bon-jovi-llega-por-primera-vez-a-cuenca">
                    <img src="https://via.placeholder.com/250x150" alt="Tributo a Bon Jovi en Cuenca">
                </a>
                <div class="card-content">
                    <h3>Banda Tributo a Bon Jovi en Cuenca</h3>
                    <p>La banda británica oficial de tributo a Bon Jovi llega por primera vez a Cuenca, ofreciendo un espectáculo inolvidable con los grandes éxitos de la legendaria banda de rock.</p>
                    <a href="https://mileniumtvi.com/la-banda-britanica-oficial-de-tributo-a-bon-jovi-llega-por-primera-vez-a-cuenca">Leer más</a>
                </div>
            </div>
            <div class="card">
                <a href="https://mileniumtvi.com/hyundai-presenta-en-cuenca-su-nueva-linea-de-camiones-mighty-e-potencia-eficiencia-y-diseno-renovado-para-el-trabajo-pesado">
                    <img src="https://via.placeholder.com/250x150" alt="Hyundai Mighty EX en Cuenca">
                </a>
                <div class="card-content">
                    <h3>Hyundai Mighty EX en Cuenca</h3>
                    <p>Hyundai presentó su renovada línea de camiones Mighty EX en Cuenca, destacando modelos como EX6, EX6 GT, EX8 y EX10 con potencia y diseño renovado.</p>
                    <a href="https://mileniumtvi.com/hyundai-presenta-en-cuenca-su-nueva-linea-de-camiones-mighty-e-potencia-eficiencia-y-diseno-renovado-para-el-trabajo-pesado">Leer más</a>
                </div>
            </div>
            <div class="card">
                <a href="https://mileniumtvi.com/obras-comprometidas-son-olvidadas-por-la-municipalidad">
                    <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/Obras-municipalidad-olvidadas.jpg" alt="Obras comprometidas">
                </a>
                <div class="card-content">
                    <h3>Obras comprometidas por la Municipalidad son olvidadas</h3>
                    <p>Proyectos prometidos por la Municipalidad no se han ejecutado, generando preocupación en la ciudadanía.</p>
                    <a href="https://mileniumtvi.com/obras-comprometidas-son-olvidadas-por-la-municipalidad">Leer más</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Noticia en Imágenes -->
    <section id="imagenes" class="section">
        <h2>Noticia en Imágenes</h2>
        <div class="grid">
            <div class="card">
                <img src="https://img.youtube.com/vi/3Ws3KFTv4pE/hqdefault.jpg" alt="Distribuidor de Tráfico Monay - ÍESS">
                <div class="card-content">
                    <h3>Distribuidor de Tráfico Monay - ÍESS</h3>
                    <p>El presidente de la República, Daniel Noboa Azín, lideró el evento simbólico de colocación de la primera piedra de la construcción del distribuidor de tráfico Monay - ÍESS ubicada en Azuay.</p>
                    <a href="https://youtu.be/3Ws3KFTv4pE" target="_blank">Ver video</a>
                </div>
            </div>
            <div class="card">
                <img src="https://img.youtube.com/vi/3Ws3KFTv4pE/hqdefault.jpg" alt="Inauguración Central Termoeléctrica El Descanso II">
                <div class="card-content">
                    <h3>Inauguración Central Termoeléctrica El Descanso II</h3>
                    <p>Este 30 de julio de 2025, el presidente de la República, Daniel Noboa Azin, inauguró la Central Termoeléctrica Terrestre El Descanso II, ubicada en el cantón Azogues, provincia del Cañar.</p>
                    <a href="https://youtu.be/z1xQfEvFjA8?si=deueu9QrihN2rcYY" target="_blank">Ver video</a>
                </div>
            </div>
            <div class="card">
                <img src="https://img.youtube.com/vi/z77l-H4H664/hqdefault.jpg" alt="Accidente en Cuenca - Girón - Pasaje">
                <div class="card-content">
                    <h3>Accidente en Cuenca - Girón - Pasaje</h3>
                    <p>2 personas fallecieron en un grave accidente de tránsito en la vía Cuenca - Girón - Pasaje este martes. Uno es un niño de 4 años de edad.</p>
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
                <iframe width="100%" height="315" src="https://www.youtube.com/embed/MHjAUKw1VAE" title="Video Viral" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                <div class="card-content">
                    <h3>Video Viral</h3>
                    <p>Mira los videos más populares de la semana.</p>
                </div>
            </div>
            <div class="card">
                <iframe width="100%" height="315" src="https://www.youtube.com/embed/WIc2_BaF0Mo?si=GMguO6tXNOpN9GYc" title="Entrevista Exclusiva" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
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
                    <img src="https://via.placeholder.com/250x150" alt="Transformación Digital en Perucho">
                </a>
                <div class="card-content">
                    <h3>Transformación Digital en Perucho</h3>
                    <p>La parroquia rural de Perucho en Quito vivió este miércoles 30 de julio, una jornada de transformación digital.</p>
                    <a href="https://mileniumtvi.com/mas-de-100-ciudadanos-de-perucho-se-certifican-en-herramientas-digitales-y-rompen-la-brecha-tecnologica">Leer más</a>
                </div>
            </div>
            <div class="card">
                <a href="https://mileniumtvi.com/el-80--de-las-enfermedades-cronicas-se-pueden-prevenir-con-autocuidadopor-ciento-">
                    <img src="https://via.placeholder.com/250x150" alt="Prevención de enfermedades crónicas">
                </a>
                <div class="card-content">
                    <h3>80% de enfermedades crónicas prevenibles con autocuidado</h3>
                    <p>Expertos destacan que el 80% de las enfermedades crónicas pueden prevenirse con prácticas de autocuidado, promoviendo hábitos saludables.</p>
                    <a href="https://mileniumtvi.com/el-80--de-las-enfermedades-cronicas-se-pueden-prevenir-con-autocuidadopor-ciento-">Leer más</a>
                </div>
            </div>
            <div class="card">
                <a href="https://mileniumtvi.com/jose-adolfo-fito-macias-villamar-lider-de-la-organizacion-criminal-transnacional-los-choneros-fue-extraditado">
                    <img src="https://via.placeholder.com/250x150" alt="Extradición de Fito Macías">
                </a>
                <div class="card-content">
                    <h3>Extradición de Fito Macías</h3>
                    <p>José Adolfo Fito Macías, líder de Los Choneros, fue extraditado, marcando un hito en la lucha contra el crimen organizado.</p>
                    <a href="https://mileniumtvi.com/jose-adolfo-fito-macias-villamar-lider-de-la-organizacion-criminal-transnacional-los-choneros-fue-extraditado">Leer más</a>
                </div>
            </div>
            <div class="card">
                <a href="https://mileniumtvi.com/ecuador-y-emiratos-arabes-unidos-fortalecen-lazos-de-cooperacion">
                    <img src="https://via.placeholder.com/250x150" alt="Artículo Especial">
                </a>
                <div class="card-content">
                    <h3>Artículo Especial</h3>
                    <p>Ecuador y Emiratos Árabes Unidos firman acuerdos para impulsar turismo, conectividad aérea y seguridad, promoviendo intercambios culturales.</p>
                    <a href="https://mileniumtvi.com/ecuador-y-emiratos-arabes-unidos-fortalecen-lazos-de-cooperacion">Leer más</a>
                </div>
            </div>
            <div class="card">
                <a href="https://mileniumtvi.com/ecuador-y-emiratos-arabes-unidos-fortalecen-lazos-de-cooperacion">
                    <img src="https://via.placeholder.com/250x150" alt="Blog del Mes">
                </a>
                <div class="card-content">
                    <h3>Blog del Mes</h3>
                    <p>Descubre cómo los lazos entre Ecuador y Emiratos Árabes abren oportunidades para el comercio y la innovación tecnológica.</p>
                    <a href="https://mileniumtvi.com/ecuador-y-emiratos-arabes-unidos-fortalecen-lazos-de-cooperacion">Leer más</a>
                </div>
            </div>
            <div class="card">
                <a href="https://mileniumtvi.com/ya-puedes-viajar-en-tren-por-la-ruta-nariz-del-diablo-de-ecuador">
                    <img src="https://via.placeholder.com/250x150" alt="Ruta Nariz del Diablo">
                </a>
                <div class="card-content">
                    <h3>Ruta Nariz del Diablo</h3>
                    <p>Ya está disponible el viaje en tren por la icónica Ruta Nariz del Diablo, ofreciendo una experiencia única en Ecuador.</p>
                    <a href="https://mileniumtvi.com/ya-puedes-viajar-en-tren-por-la-ruta-nariz-del-diablo-de-ecuador">Leer más</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Defensa del Televidente -->
    <section id="defensa" class="section">
        <h2>Defensa del Televidente</h2>
        <p>En nuestro canal, tu voz importa. Contáctanos para cualquier queja, sugerencia o consulta.</p>
        <form>
            <input type="text" placeholder="Nombre" required>
            <input type="email" placeholder="Correo Electrónico" required>
            <textarea placeholder="Tu mensaje" required></textarea>
            <button type="submit">Enviar</button>
        </form>
    </section>

    <!-- Footer -->
    <footer>
        <p>© 2025 Canal de TV. Todos los derechos reservados.</p>
        <p><a href="#">Términos y Condiciones</a> | <a href="#">Política de Privacidad</a> | <a href="#defensa">Contacto</a></p>
        <div class="social">
            <a href="https://www.facebook.com/mileniumtvi/" target="_blank"><i class="fab fa-facebook-f"></i></a>
            <a href="https://x.com/mileniumtvi" target="_blank"><i class="fab fa-x-twitter"></i></a>
            <a href="#"><i class="fab fa-instagram"></i></a>
            <a href="https://www.youtube.com/@mileniumtvi" target="_blank"><i class="fab fa-youtube"></i></a>
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
    </script>
</body>
</html>

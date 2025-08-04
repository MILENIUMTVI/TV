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
            overflow-x: hidden; /* Evita desbordamiento horizontal */
        }

        .header-container {
            max-width: 1200px;
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
            gap: 1.5rem;
            align-items: center; /* Alinea verticalmente los elementos del menú */
            flex-wrap: wrap; /* Permite que los elementos se ajusten en varias líneas si es necesario */
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s;
            line-height: 1; /* Normaliza altura de línea */
            white-space: nowrap; /* Evita división de texto */
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
            padding: 3rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section h2 {
            font-size: 2rem;
            margin-bottom: 1.5rem;
            color: #ffd700; /* Amarillo dorado igual que footer a */
        }

        #live h2 {
            color: #1a73e8; /* Azul original para Transmisiones en Vivo */
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
            gap: 1.5rem;
        }

        .entrevistas-container .video-wrapper {
            position: relative;
            width: 100%;
            max-width: 800px;
            padding-bottom: 56.25%; /* Mantiene proporción 16:9 */
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
            font-size: 1rem;
            color: #333;
            max-width: 800px;
            text-align: center;
        }

        /* Footer */
        footer {
            background: #0d47a1;
            color: white;
            padding: 2rem;
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
                font-size: 2rem;
            }

            nav ul {
                flex-direction: column;
                gap: 0.8rem; /* Reducido para evitar desbordamiento */
                align-items: center; /* Mantener alineación en vista móvil */
            }

            nav ul li a {
                font-size: 0.9rem; /* Tamaño de fuente reducido para vista móvil */
                padding: 0.5rem; /* Añade algo de padding para mejor legibilidad */
            }

            .live-stream .video-js {
                height: 300px;
            }

            .entrevistas-container .video-wrapper {
                max-width: 100%;
                padding-bottom: 56.25%; /* Mantener proporción 16:9 */
            }

            .entrevistas-container p {
                font-size: 0.9rem;
                padding: 0 1rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="header-container">
            <!-- Logo retirado según instrucción -->
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
        <video
            id="live-stream-player"
            class="video-js vjs-default-skin"
            controls
            preload="auto"
            width="800"
            height="450"
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
                    allowfullscreen>
                </iframe>
            </div>
            <p>La SEPS dispone la suspensión de operaciones y liquidación forzosa de la Cooperativa CREA Ltda. y garantiza la protección de los depósitos de los socios.</p>
            <div class="video-wrapper">
                <iframe
                    src="https://www.youtube.com/embed/pOYq1aaJHRk?si=B2nBmp5UC2dI_p0I"
                    title="Entrevista al Presidente de Ecuador Daniel Noboa Azín"
                    frameborder="0"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                    allowfullscreen>
                </iframe>
            </div>
            <p>Entrevista al Presidente de Ecuador Daniel Noboa Azín</p>
            <div class="video-wrapper">
                <iframe
                    src="https://www.youtube.com/embed/JReQmALQX4g?si=hhV0Z35AOG7uGafi"
                    title="Entrevista Exclusiva"
                    frameborder="0"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                    allowfullscreen>
                </iframe>
            </div>
            <p>El analista Hernán Bravo Ordóñez experto en Economía y Finanzas se pregunta:  ¿Habrá más apagones en Ecuador? Un interesante análisis.</p>
        </div>
    </section>

    <!-- TV Play -->
    <section id="tvplay" class="section">
        <h2>TV Play</h2>
        <div class="grid">
            <div class="card">
                <iframe width="100%" height="315" src="https://www.youtube.com/embed/xc4BXbdbPgk?si=jCPAkkJu3cfYakvQ" title="Programa Estelar" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                <div class="card-content">
                    <h3>Programa Estelar</h3>
                    <p>Disfruta de nuestro programa insignia con invitados especiales.</p>
                </div>
            </div>
            <div class="card">
                <iframe width="100%" height="315" src="https://www.youtube.com/embed/QRV5teEvBlY?si=21Sz5Mp5ZkxKiV1W" title="Serie Exclusiva" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                <div class="card-content">
                    <h3>Serie Exclusiva</h3>
                    <p>Una serie que no te puedes perder, disponible en TV Play.</p>
                </div>
            </div>
            <div class="card">
                <iframe width="100%" height="315" src="https://app.viloud.tv/watch/video/b3716180466af9bbf2aa867df20eaa13" title="Noticiero de Ecuador TV" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                <div class="card-content">
                    <h3>Noticiero de Ecuador TV</h3>
                    <p>Noticiero de Ecuador TV 31 de julio de 2025.</p>
                </div>
            </div>
            <div class="card">
                <iframe width="100%" height="315" src="https://app.viloud.tv/watch/video/416f5c45086bb542102c47b546c2a77b" title="Viaje al centro de la tele - Los Reyes del popurrí" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen data-setup='{"autoplay": false}'></iframe>
                <div class="card-content">
                    <h3>Viaje al centro de la tele - Los Reyes del popurrí</h3>
                    <p>Viaje al centro de la tele - Los Reyes del popurrí.</p>
                </div>
            </div>
            <div class="card">
                <iframe width="100%" height="315" src="https://app.viloud.tv/watch/video/c92246b4b186fc745838ce0d162bf6d9" title="Noticiero DW" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen data-setup='{"autoplay": false}'></iframe>
                <div class="card-content">
                    <h3>Noticiero DW</h3>
                    <p>SW Noticias 4 de agosto 2025.</p>
                </div>
            </div>
            <div class="card">
                <iframe width="100%" height="315" src="https://app.viloud.tv/watch/video/6d8edbaa8833d5ceed9d4d53402db27a" title="Telediario" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen data-setup='{"autoplay": false}'></iframe>
                <div class="card-content">
                    <h3>Telediario</h3>
                    <p>Noticiero RTVE 4 de agosto 2025.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Noticias -->
    <section id="news" class="section">
        <h2>Noticias</h2>
        <div class="grid">
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
            <div class="card">
                <img src="https://via.placeholder.com/250x150" alt="Cooperación con EE.UU.">
                <div class="card-content">
                    <h3>El gobierno de Noboa fortalece la cooperación con EE.UU.</h3>
                    <p>El gobierno de Daniel Noboa consolida la alianza con EE.UU. mediante acuerdos en seguridad, comercio y desarrollo, promoviendo beneficios mutuos y fortaleciendo la cooperación bilateral.</p>
                    <a href="https://mileniumtvi.com/el-gobierno-de-noboa-fortalece-la-cooperacion-con-eeuu" target="_blank">Leer más</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Noticias Locales -->
    <section id="locales" class="section">
        <h2>Noticias Locales</h2>
        <div class="grid">
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
                <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/Bloque-de-seguridad-Duran.jpg" alt="3er Festival de la Fritada en Sidcay">
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
                <iframe width="100%" height="315" src="https://www.youtube.com/embed/MHjAUKw1VAE" title="Video Viral" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                <div class="card-content">
                    <h3>Video Viral</h3>
                    <p>Mira los videos más populares de la semana.</p>
                </div>
            </div>
            <div class="card">
                <iframe width="100%" height="315" src="https://www.youtube.com/embed/WIc2_BaF0Mo?si=GMguO6tXNOpN9GYc" title="Entrevista Exclusiva" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
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
                    <img src="https://tu-servidor.com/imagenes/articulo-ecuador-emiratos.jpg" alt="Artículo Especial">
                </a>
                <div class="card-content">
                    <h3>Artículo Especial</h3>
                    <p>Ecuador y Emiratos Árabes Unidos firman acuerdos para impulsar turismo, conectividad aérea y seguridad, promoviendo intercambios culturales.</p>
                    <a href="https://mileniumtvi.com/ecuador-y-emiratos-arabes-unidos-fortalecen-lazos-de-cooperacion">Leer más</a>
                </div>
            </div>
            <div class="card">
                <a href="https://mileniumtvi.com/ecuador-y-emiratos-arabes-unidos-fortalecen-lazos-de-cooperacion">
                    <img src="https://tu-servidor.com/imagenes/articulo-ecuador-emiratos.jpg" alt="Blog del Mes">
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

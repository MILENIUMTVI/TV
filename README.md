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
                gap: 1rem;
                align-items: center; /* Mantener alineación en vista móvil */
            }

            .live-stream .video-js {
                height: 300px;
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

    <!-- TV Play -->
    <section id="tvplay" class="section">
        <h2>TV Play</h2>
        <div class="grid">
            <div class="card">
                <img src="https://www.canva.com/design/DAGrNUbFdSQ/O2JWkQP-9spi5KLvdhz-3Q/view?utm_content=DAGrNUbFdSQ&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=h5670f93789" alt="Programa 1">
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
        </div>
    </section>

    <!-- Noticias -->
    <section id="news" class="section">
        <h2>Noticias</h2>
        <div class="grid">
            <!-- Nueva noticia 1 -->
            <div class="card">
                <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/Bloque-de-seguridad-Duran.jpg" alt="Sistemas de Agua Potable y Alcantarillado">
                <div class="card-content">
                    <h3>Sistemas de Agua Potable y Alcantarillado para Baba</h3>
                    <p>Se implementan nuevos sistemas de agua potable y alcantarillado pluvial en Baba para mejorar la calidad de vida y la infraestructura local.</p>
                    <a href="https://mileniumtvi.com/sistemas-de-agua-potable-y-alcantarillado-pluvial-para-baba" target="_blank">Leer más</a>
                </div>
            </div>
            <!-- Nueva noticia 2 -->
            <div class="card">
                <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/Bloque-de-seguridad-Duran.jpg" alt="Gobierno Firme Contra el Crimen">
                <div class="card-content">
                    <h3>El Gobierno Nacional Firme Contra el Crimen</h3>
                    <p>El gobierno nacional refuerza medidas contra el crimen organizado, implementando estrategias para garantizar la seguridad ciudadana.</p>
                    <a href="https://mileniumtvi.com/el-gobierno-nacional-firme-contra-el-crimen" target="_blank">Leer más</a>
                </div>
            </div>
            <!-- Nueva noticia 3 -->
            <div class="card">
                <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/Bloque-de-seguridad-Duran.jpg" alt="3er Festival de la Fritada en Sidcay">
                <div class="card-content">
                    <h3>Sidcay se llenará de sabor con el 3er Festival de la Fritada</h3>
                    <p>El 3er Festival de la Fritada en Sidcay promete deleitar a los asistentes con gastronomía, música y actividades culturales para toda la familia.</p>
                    <a href="https://mileniumtvi.com/sidcay-se-llenara-de-sabor-con-el-3er-festival-de-la-fritada" target="_blank">Leer más</a>
                </div>
            </div>
            <!-- Nueva noticia destacada -->
            <div class="card">
                <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/Bloque-de-seguridad-Duran.jpg" alt="Operativo en Recinto Ferial">
                <div class="card-content">
                    <h3>Operativo en Recinto Ferial</h3>
                    <p>Operativo de control en los alrededores del Recinto Ferial El Arenal.</p>
                    <a href="https://mileniumtvi.com/operativo-de-control-en-los-alrededores-del-recinto-ferial-el-arenal" target="_blank">Leer más</a>
                </div>
            </div>
            <!-- Nueva noticia 1 -->
            <div class="card">
                <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/Bloque-de-seguridad-Duran.jpg" alt="Reactivación del SOTE">
                <div class="card-content">
                    <h3>Gobierno anuncia reactivación del SOTE</h3>
                    <p>El gobierno anuncia la reactivación del SOTE este 17 de julio y un plan de mantenimiento estructural.</p>
                    <a href="https://mileniumtvi.com/gobierno-anuncia-reactivacion-del-sote-este-17-de-julio-y-un-plan-de-mantenimiento-estructural" target="_blank">Leer más</a>
                </div>
            </div>
            <!-- Nueva noticia 2 -->
            <div class="card">
                <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/Bloque-de-seguridad-Duran.jpg" alt="Condecoración a Daniel Noboa">
                <div class="card-content">
                    <h3>Jóvenes condecoran a Daniel Noboa</h3>
                    <p>Jóvenes estudiantes condecoran al presidente Daniel Noboa por las más de 409.000 becas entregadas en su gestión.</p>
                    <a href="https://mileniumtvi.com/jovenes-estudiantes-condecoran-al-presidente-daniel-noboa" target="_blank">Leer más</a>
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
                <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/Bloque-de-seguridad-Duran.jpg" alt="Retiro de Firmas RC5">
                <div class="card-content">
                    <h3>Retiro de Firmas RC5</h3>
                    <p>Cuatro Asambleístas de RC5 han retirado su firma del proyecto de ley presentado por su ex compañero de bancada Santiago Díaz en el que se propone que el consentimiento para una relación sexual sea a partir de los 14 años y no desde los 18.</p>
                    <a href="https://mileniumtvi.com/ex-companeros-de-la-bancada-la-revolucion-ciudadana-comenzaron-a-retirar-sus-firmas" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/Bloque-de-seguridad-Duran.jpg" alt="Relevo de Mando Policial">
                <div class="card-content">
                    <h3>Relevo de Mando Policial</h3>
                    <p>El presidente Daniel Noboa oficializó el relevo del mando policial: Pablo Dávila es el nuevo Comandante General.</p>
                    <a href="https://mileniumtvi.com/el-presidente-daniel-noboa-oficializo-el-relevo-del-mando-policial-pablo-davila-es-el-nuevo-comandante-general" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/Bloque-de-seguridad-Duran.jpg" alt="Caso Santiago Díaz">
                <div class="card-content">
                    <h3>Caso Santiago Díaz</h3>
                    <p>Santiago Díaz era el legislador alterno de Priscila Schettini, y se principalizó luego de que a Schettini se le suspendieran sus derechos políticos. Está acusado de violación a una menor.</p>
                    <a href="https://mileniumtvi.com/santiago-diaz-era-el-legislador-alterno-de-priscila-schettini-y-se-principalizo-luego-de-que-a-schettini-se-le-suspendieran-sus-derechos-politicos-esta-acusado-de-violacion-a-una-menor" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/Bloque-de-seguridad-Duran.jpg" alt="Lucha contra la corrupción">
                <div class="card-content">
                    <h3>La lucha contra la corrupción continúa</h3>
                    <p>El bloque de seguridad interviene cinco instituciones públicas en Durán.</p>
                    <a href="https://mileniumtvi.com/la-lucha-contra-la-corrupcion-continua-el-bloque-de-seguridad-interviene-cinco-instituciones-publicas-en-duran" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/Presidente-Noboa-reuniones-italianas.jpg" alt="Noticia Destacada">
                <div class="card-content">
                    <h3>Noticia Destacada</h3>
                    <p>Presidente Noboa mantuvo reuniones bilaterales con las máximas autoridades de la política italiana para fortalecer cooperación y seguridad.</p>
                    <a href="https://mileniumtvi.com/presidente-noboa-mantuvo-reuniones-bilaterales-con-las-maximas-autoridades-de-la-politica-italiana" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://img.youtube.com/vi/U9X45mxZcls/hqdefault.jpg" alt="Noticia Local">
                <div class="card-content">
                    <h3>Noticia Local</h3>
                    <p>Eventos comunitarios destacados captados en video, mostrando la riqueza cultural y social de nuestra región.</p>
                    <a href="https://youtu.be/U9X45mxZcls?si=h68Vp7W9HZPJmf48" target="_blank">Ver video</a>
                </div>
            </div>
            <div class="card">
                <img src="https://www.canva.com/design/DAGrNUMTC64/a-pMihPoo9L1C55W5vU0jg/watch?utm_content=DAGrNUMTC64&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=h3ea15cd559" alt="Editorial">
                <div class="card-content">
                    <h3>Editorial</h3>
                    <p>Explora las opiniones y análisis de nuestros expertos sobre los temas más relevantes.</p>
                    <a href="https://mileniumtvi.com/opinion" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://mileniumtvi.com/wp-content/uploads/2025/06/Empresarios-italianos.jpg" alt="Noticia Empresarios Italianos">
                <div class="card-content">
                    <h3>Empresarios Italianos y Presidente Noboa</h3>
                    <p>Empresarios italianos dialogaron con el Presidente Daniel Noboa sobre inversiones en sectores estratégicos.</p>
                    <a href="https://mileniumtvi.com/empresarios-italianos-en-areas-estrategicas-dialogaron-con-el-presidente-daniel-noboa-sobre-inversion-en-sectores-estrategicos" target="_blank">Leer más</a>
                </div>
            </div>
            <div class="card">
                <img src="https://pbs.twimg.com/media/GvXiaxLXEAAFS-9.jpg?format=jpg&name=small" alt="Caso de Violación">
                <div class="card-content">
                    <h3>Caso de Violación a Menor</h3>
                    <p>Una menor de apenas 12 años, presuntamentre fue víctima de violación por parte de un sujeto identificado como Joseph Santiago Díaz Asque RC5, el reemplazo de Prisclila Schettini en la Asamblea del enlace <a href="https://x.com/mileniumtvi/status/1942707934242169275">https://x.com/mileniumtvi/status/1942707934242169275</a></p>
                </div>
            </div>
        </div>
    </section>

    <!-- Noticia en Imágenes -->
    <section id="imagenes" class="section">
        <h2>Noticia en Imágenes</h2>
        <div class="grid">
            <div class="card">
                <img src="https://via.placeholder.com/250x150" alt="Ceremonia de Cambio de Mando">
                <div class="card-content">
                    <h3>Ceremonia de Cambio de Mando</h3>
                    <p><a href="https://mileniumtvi.com/ceremonia-de-cambio-de-mando-policial-quito-09072025" target="_blank">https://mileniumtvi.com/ceremonia-de-cambio-de-mando-policial-quito-09072025</a></p>
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
                <a href="https://mileniumtvi.com/obras-comprometidas-son-olvidadas-por-la-municipalidad">
                    <img src="https://mileniumtvi.com/wp-content/uploads/2025/07/Obras-municipalidad-olvidadas.jpg" alt="Obras comprometidas">
                </a>
                <div class="card-content">
                    <h3>Obras comprometidas por la Municipalidad son olvidadas</h3>
                    <p>Proyectos prometidos por la Municipalidad no se han ejecutado, generando preocupación en la ciudadanía.</p>
                    <a href="https://mileniumtvi.com/obras-comprometidas-son-olvidadas-por-la-municipalidad">Leer más</a>
                </div>
            </div>
            <div class="card">
                <a href="https://mileniumtvi.com/ecuador-y-emiratos-arabes-unidos-fortalecen-lazos-de-cooperacion">
                    <img src="https://tu-servidor.com/imagenes/articulo-ecuador-emiratos.jpg" alt="Artículo Especial">
                </a>
                <div class="card-content">
                    <h3>Artículo Especial</h3>
                    <p>Ecuador y Emiratos Árabes Unidos firman acuerdos para impulsar turismo, conectividad aérea y seguridad, promoviendo intercambios culturales y comerciales.</p>
                    <a href="https://mileniumtvi.com/ecuador-y-emiratos-arabes-unidos-fortalecen-lazos-de-cooperacion">Leer más</a>
                </div>
            </div>
            <div class="card">
                <a href="https://mileniumtvi.com/ecuador-y-emiratos-arabes-unidos-fortalecen-lazos-de-cooperacion">
                    <img src="https://tu-servidor.com/imagenes/articulo-ecuador-emiratos.jpg" alt="Blog del Mes">
                </a>
                <div class="card-content">
                    <h3>Blog del Mes</h3>
                    <p>Descubre cómo los nuevos lazos entre Ecuador y Emiratos Árabes abren oportunidades para el comercio y la innovación tecnológica.</p>
                    <a href="https://mileniumtvi.com/ecuador-y-emiratos-arabes-unidos-fortalecen-lazos-de-cooperacion">Leer más</a>
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

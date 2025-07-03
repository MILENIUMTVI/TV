# TV
MILENIUM TELEVISION INTERNACIONAL
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
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s;
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
            <div class="logo">
                <img src="logomtvi.png/header_photo" alt="Logo Canal TV">
            </div>
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

<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Restaurante Wassim El Bouhoutani</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f7f7f7;
            color: #333;
            line-height: 1.6;
        }
        header {
            background: linear-gradient(45deg, #FFEA00, #FFC107); /* Amarillo más suave */
            color: white;
            text-align: center;
            padding: 40px 0;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        h1 {
            font-size: 3.5rem;
            margin: 0;
            text-transform: uppercase;
            letter-spacing: 3px;
            font-family: 'Helvetica', sans-serif;
            color: #004B87; /* Azul oscuro */
            display: inline-block; /* Para permitir que la imagen esté al lado */
        }
        .pizza-image {
            height: 80px; /* Ajustar el tamaño de la imagen */
            vertical-align: middle; /* Alinear verticalmente con el texto */
            margin-left: 20px; /* Espacio entre el título y la imagen */
        }
        h2 {
            font-size: 2.5rem;
            margin-top: 10px;
            text-transform: uppercase;
            color: #FF5733;
        }
        .instagram-link {
            font-size: 1.2rem;
            color: #FF6F20; /* Naranja vibrante */
            text-decoration: underline;
            margin-top: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .instagram-link img {
            width: 24px; /* Tamaño del icono */
            margin-right: 8px; /* Espacio entre icono y texto */
        }
        nav {
            margin: 15px 0;
        }
        nav a {
            color: white;
            margin: 0 20px;
            text-decoration: none;
            font-weight: bold;
            text-transform: uppercase;
            font-size: 1.1rem;
        }
        nav a:hover {
            text-decoration: underline;
        }
        .menu {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            padding: 50px 20px;
        }
        .menu-item {
            border-radius: 20px;
            margin: 20px;
            padding: 30px;
            width: 300px;
            text-align: center;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
            cursor: pointer;
            color: white; /* Texto en blanco por defecto */
        }
        .menu-item:hover {
            transform: translateY(-12px);
            box-shadow: 0 15px 35px rgba(0,0,0,0.2);
        }
        .menu-item img {
            width: 100%;
            height: auto;
            border-radius: 15px;
            transition: opacity 0.3s ease-in-out;
        }
        .menu-item img:hover {
            opacity: 0.85;
        }
        .menu-item h3 {
            margin: 20px 0;
            font-size: 1.85rem;
        }
        .menu-item p {
            font-size: 1.1rem;
            margin: 10px 0 25px;
        }
        
        /* Estilos específicos para cada restaurante */
        .mcdonalds {
            background-color: #6DBE45; /* Verde McDonald's */
        }

        .burger-king {
            background-color: #FEDD00; /* Amarillo Burger King */
            color: black; /* Texto en negro */
        }

        .kfc {
            background-color: #A52A2A; /* Marrón KFC */
        }

        .dominos {
            background-color: #004B87; /* Azul Domino's Pizza */
        }

        footer {
            text-align: center;
            padding: 30px;
            background-color: #FFC300;
            color: black;
            box-shadow: 0 -2px 10px rgba(0,0,0,0.1);
            width: 100%;
            margin-top: 50px;
        }
        footer p {
            margin: 0;
            font-size: 1rem;
            letter-spacing: 1px;
        }
        footer a {
            color: black;
            font-weight: bold;
            text-decoration: none;
        }
        footer a:hover {
            text-decoration: underline;
        }
        @media screen and (max-width: 768px) {
            .menu-item {
                width: 90%;
                margin: 15px 0;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Restaurante Wassim El Bouhoutani</h1>
        <img class="pizza-image" src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a7/Pizza_Slice.png/512px-Pizza_Slice.png" alt="Pizza Domino's" /> <!-- URL de la imagen de pizza -->
        <h2>Fast Food King</h2>
        <p class="instagram-link">
            <img src="https://upload.wikimedia.org/wikipedia/commons/a/a5/Instagram_icon.png" alt="Instagram" />
            Síguenos en Instagram: <a href="https://www.instagram.com/wassim_ebea/" target="_blank">@wassim_ebea</a>
        </p>
        <nav>
            <a href="#">Inicio</a>
            <a href="#">Menú</a>
            <a href="#">Reservas</a>
            <a href="#" onclick="openContactModal()">Contacto</a>
        </nav>
    </header>

    <section class="menu">
        <!-- McDonald's -->
        <div class="menu-item mcdonalds" onclick="window.location.href='https://www.mcdonalds.es';">
            <img src="mcdonalds.jpg" alt="McDonald's">
            <h3>McDonald's</h3>
            <p>Elige tus hamburguesas favoritas.</p>
        </div>

        <!-- Burger King -->
        <div class="menu-item burger-king" onclick="window.location.href='https://www.burgerking.es';">
            <img src="burgerking.jpg" alt="Burger King">
            <h3>Burger King</h3>
            <p>Disfruta de Whoppers y más.</p>
        </div>

        <!-- KFC -->
        <div class="menu-item kfc" onclick="window.location.href='https://www.kfc.es';">
            <img src="kfc.jpg" alt="KFC">
            <h3>KFC</h3>
            <p>Pollo frito que te encantará.</p>
        </div>

        <!-- Domino's Pizza -->
        <div class="menu-item dominos" onclick="window.location.href='https://www.dominospizza.es';">
            <img src="dominos.jpg" alt="Domino's Pizza">
            <h3>Domino's Pizza</h3>
            <p>La mejor pizza a domicilio.</p>
        </div>
    </section>

    <footer>
        <p>&copy; 2024 Restaurante Wassim El Bouhoutani. Todos los derechos reservados. <a href="#">Términos y condiciones</a> | <a href="#">Política de privacidad</a></p>
    </footer>

    <!-- Modal para contacto -->
    <div class="modal" id="contactModal">
        <div class="modal-content">
            <span class="close-modal">&times;</span>
            <h2>Contacto</h2>
            <p>Síguenos en Instagram: <a href="https://www.instagram.com/wassim_ebea/" target="_blank">@wassim_ebea</a></p>
        </div>
    </div>

    <script>
        function openContactModal() {
            document.getElementById('contactModal').style.display = 'flex';
        }

        document.querySelectorAll('.close-modal').forEach(function(el) {
            el.onclick = function() {
                document.getElementById('contactModal').style.display = 'none';
            };
        });
    </script>
</body>
</html>

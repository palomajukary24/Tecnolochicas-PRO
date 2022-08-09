<!DOCTYPE html>
<html lang="es">
<head>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Roboto&display=swap" rel="stylesheet">
    <link href="https://cdn.lineicons.com/3.0/lineicons.css" rel="stylesheet">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Ejemplo layout flexbox</title>
    <style>
        html, body {
            display: flex;
            flex-direction: column;
            height: 100%;
        }

        body {
            margin: 0;
            background: #F09281;
            color: #030201;
            font-family: 'Arial', sans-serif;
        }

        #header {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        #navigation-bar ul {
            margin: 0;
            padding: 0;
            border: 1px solid #e7e7e7;
            background-color: #f3f3f3;
        }

        #navigation-bar li {
            display: inline-block;
        }

        #navigation-bar li a {
            display: block;
            color: #665;
            text-align: center;
            padding: 14px 16px;
            text-decoration: none;
        }

        #navigation-bar li a:hover:not(.active) {
            background-color: #ddd;
        }

        #navigation-bar li a.active {
            color: #fff;
            background-color: #665;
        }

        #navigation-bar .menu__hamburger-icon {
            display: none;
        }

        @media screen and (max-width: 600px) {
            #navigation-bar li:not(:first-child) {
                display: none;
            }
            #navigation-bar li.menu__hamburger-icon {
                display: block;
                float: right;
            }
            #navigation-bar.responsive {
                position: relative;
            }
            #navigation-bar.responsive .menu__hamburger-icon {
                position: absolute;
                right: 0;
                top: 0;
            }
            #navigation-bar.responsive .menu__hamburger-icon a {
                color: #fff;
            }
            #navigation-bar.responsive li {
                float: none;
                display: block !important;
            }
            #navigation-bar.responsive li a{
                text-align: left;
            }
        }

        #main-content-container {
            display: flex;
        }

        #links-sidebar {
            flex: 2;
            background: pink
        }

        #main-content {
            flex: 6;
            padding: 10px 20% 10px 10px;
        }

        .main-content__img--full-width {
            width: 100%;
        }

        #footer {
            padding: 0 10px 10px 10px;
            margin-top: auto;
            display: flex;
            background: #f3f3f3;
        }

        .footer__section {
            flex: 1;
            display: flex;
            align-items: center;
            flex-direction: column;
        }

        .social__networks {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .social__network {
            display: flex;
            align-items: center;
        }

        .social__icon {
            font-size: 32px;
        }

        .social__icon-handler {
            margin-left: 10px;
        }

        input[type=email], textarea {
            width: 100%;
            padding: 12px 20px;
            margin: 8px 0;
            box-sizing: border-box;
            border: 3px solid #ccc;
            transition: 0.5s;
            outline: none;
        }

        input[type=email]:focus, textarea:focus {
            border: 3px solid #555;
        }

        input[type=submit] {
            background: #666655;
            border: none;
            color: white;
            padding: 16px 32px;
            text-decoration: none;
            margin: 4px 2px;
            cursor: pointer;
        }

        a{
            text-decoration: none;
            color: inherit;
        }

        a:hover {
            text-decoration: underline;
            text-underline-offset: 3px;
        }

    </style>

    <script>
        function myFunction() {
            const navigationBar = document.getElementById("navigation-bar");
            if (navigationBar.className === "navigation-bar") {
                navigationBar.className += " responsive";
            } else {
                navigationBar.className = "navigation-bar";
            }
        }
    </script>
</head>
<body>
<header id="header">
    <h1> David Card </h1>
    <p>1956 (edad 66 años)</p>
</header>

<nav id="navigation-bar" class="navigation-bar">
    <ul>
        <li> <a class="active" href="file:///C:/Users/paled/OneDrive/Escritorio/Documentos/web%20development%20bootcamp/Mi%20pagina%20web%204.0.html"> Principal </a></li>
        <li> <a class="active" href="https://es.wikipedia.org/wiki/David_Card#:~:text=2%20V%C3%A9ase%20tambi%C3%A9n-,Biograf%C3%ADa,1997%2C%20fue%20coeditor%20de%20Econometrica."> Wikipedia </a></li>
        <li> <a class="active" href="https://www.premiosfronterasdelconocimiento.es/galardonados/david-card/"> PREMIOS FRONTERAS DEL CONOCIMIENTO </a></li>
        <li> <a class="active" href=" https://davidcard.berkeley.edu/"> Pagina David Card en Ingles </a></li>
        
        <li class="menu__hamburger-icon">
            <a  href="javascript:void(0);" onclick="myFunction()">
                <i class="lni lni-menu"></i>
            </a>
        </li>
    </ul>
</nav>

<div id="main-content-container">
    <aside id="links-sidebar">
        Links relacionados
        <br>
      <li> <a class="active" href="https://es.wikipedia.org/wiki/David_Card#:~:text=2%20V%C3%A9ase%20tambi%C3%A9n-,Biograf%C3%ADa,1997%2C%20fue%20coeditor%20de%20Econometrica."> Wikipedia </a></li>
      <li> <a class="active" href="https://www.premiosfronterasdelconocimiento.es/galardonados/david-card/"> PREMIOS FRONTERAS DEL CONOCIMIENTO </a></li>
      <li> <a class="active" href=" https://davidcard.berkeley.edu/"> Pagina David Card en Ingles </a></li>
</aside>
    <section id="main-content">
     <img src="C:\Users\paled\OneDrive\Escritorio\Documentos/DavidCard1.jpg"" alt="David Card" class="main-content__img--full-width">

     <h2>Biografía</h2>
      <p> Card se graduó en Bachelor of Arts por la Universidad de Queen (Ontario) en 1978 y se doctoró en Economía 
          en 1983 por la Universidad de Princeton, en Estados Unidos.</p>
      <p> Entre 1988 y 1992, fue editor asociado de la Journal of Labor Economics y de 1993 a 1997, fue coeditor de 
          Econometrica. Recibió en 1995, la Medalla John Bates Clark. En 2009 fue designado para dar la Conferencia 
          Richard T. Ely de la Asociación estadounidense de economía, en San Francisco y en 2014 fue elegido 
          vicepresidente de esta misma asociación, junto a Gregory Mankiw.</p>    
        <p> A principios de 1990, Card fue centro de atención, junto a Alan B. Krueger, por sus investigaciones que
            concluían que contrariamente al pensamiento ampliamente aceptado entre los economistas, el aumento del 
            salario mínimo en Nueva Jersey no se había traducido en una reducción de puestos de trabajo de las empresas 
            de comida rápida de ese estado.2​3​ Aunque la metodología utilizada y su afirmación ha sido cuestionada por 
            algunos economistas, otros muchos, entre los que se incluye Joseph Stiglitz, han aceptado los resultados de 
            Card y Krueger. </p>
        <p> David Card también ha hecho contribuciones fundamentales a la investigación en materia de migración, 
            educación,​ formación profesional y desigualdad. Sobre la inmigración, la investigación de Card ha demostrado 
            que el impacto económico de los nuevos inmigrantes es mínima. Card ha realizado diversos estudios de casos 
            sobre la rápida asimilación de los grupos de inmigrantes, encontrando que tienen un impacto mínimo sobre los
            salarios. En una entrevista con el New York Times, Card manifestaba: Sinceramente, creo que los argumentos 
            económicos contra la inmigración son de segundo orden. Son casi irrelevante.​ Esto no implica, sin embargo,
            que Card crea que la inmigración se deba aumentar, simplemente que los inmigrantes no representan una amenaza 
            para el mercado de trabajo.</p>
        <p> A pesar de que algunas de sus investigaciones tienen fuertes implicaciones políticas, Card no ha tomado 
            públicamente una posición sobre cuestiones políticas ni ha hecho sugerencias en este ámbito. Sin embargo su 
            obra es citada regularmente en apoyo del aumento de la inmigración y la legislación sobre salario mínimo.</p>

        <p> Recibió junto a Richard Blundell el Premio Fundación BBVA Fronteras del Conocimiento 2014 en la categoría de 
            Economía, Finanzas y Gestión de Empresas por “sus contribuciones a la microeconomía empírica”, según señala 
            el acta del jurado. Partiendo de importantes problemas económicos de tipo empírico, desarrollaron y estimaron 
            modelos econométricos apropiados para estas cuestiones, llevando a cabo en ese proceso contribuciones 
            metodológicas muy significativas. Ambos se caracterizan por prestar una gran atención a aspectos institucionales,
            por sus diseños de investigación precisos e innovadores, su rigurosa aplicación de las herramientas económicas y
            por la presentación imparcial de los resultados obtenidos, continúa. </p>

        <p> En 2021 recibió el Premio Nobel de Economía «por sus contribuciones empíricas a la economía laboral» junto con 
            Joshua Angrist y Guido W. Imbens. Le correspondió la mitad del premio. </p>
        <h2> Reconocimientos</h2>
        <ul>
              <il> Medalla John Bates Clark en 1995 </il>
              <br>
              <il> Premio Fundación BBVA Fronteras del Conocimiento en 2014 </il>
           
        </ul>
        <h2> Ocupaciones </h2>
        <ul>
              <il> Economista </il>
              <br>
              <il> Profesor </il>
              <br>
              <il> Universitario </il>
              <br>
              <il> Catedrático </il>
        </ul>
        <h2> ¿Porque elegiste este personaje para tu pagina tributo? </h2>
        <p> Realmente porque es una persona estudiosa con su profesion en economía y me gustaría algun día tener una profesion
            relacionada en ese campo laboral, investigando más sobre el podría seguir avanzando con mis conocimientos en finanzas
            para que en un futuro tenga más idea sobre en lo que me quiero especializar </p>
       <p> Además hacer esta página web aprendiendo sobre muchas cosaas sobre la programación y como se utiliza este lenguaje HTML
           conjugando un tema de interes mío, se hace una experiencia increíble. </p>
       <p> Paloma Jukary Espinosa Carbajal / Estado de México, México </p>
    </section>
</div>

<footer id="footer">
    <div class="footer__social footer__section">
        <h2>Mis redes</h2>

        <div class="social__networks">
            <div class="social__network">
                <span class="social__icon-container"><i class="lni lni-linkedin-original social__icon"></i></span>
                <span class="social__icon-handler"> <a href="https://mx.linkedin.com/"> Likendin </a> </span>
            </div>

            <div class="social__network">
                <span class="social__icon-container"><i class="lni lni-github-original social__icon"></i></span> </i></span>
                <span class="social__icon-handler">
                    <a href="https://github.com/wizelineacademy/web-development-bootcamp-course"> Github </a>
                </span>
           </div>
        </div>

    </div>
    <div class="footer__contact-form footer__section">
        <h2>Contacto</h2>
        <div>
            <form>
                <label for="contactEmail"> Correo electronico:</label>
                <input id="contactEmail" required type="email" placeholder="Ingresa tu correo electronico">

                <label for="contactMessage"> Mensaje:</label>
                <textarea id="contactMessage" required rows="2" cols="20"> </textarea>

                <input type="submit" value="Enviar">
            </form>
        </div>
    </div>
    <div class="footer__more-sites footer__section">
        <h2>Otros de mis sitios</h2>
            <ul>
              <ol> Sitio one </ol>
              <ol> Sitio two </ol>
              <ol> Sitio three </ol>
              <ol> Sitio four </ol>
              <ol> Sitio five </ol>
              <ol> Sitio six </ol>
           </ul>
    </div>
</footer>
</body>
</html>

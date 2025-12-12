<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Página con tres columnas</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
/* =======================
   ESTILOS GENERALES
   ======================= */

/* --- ENCABEZADO INICIO --- */
#inicio-section h1 {
  font-family: 'Arial Black', Gadget, sans-serif; /* Fuente más gruesa y llamativa */
  font-size: 36px; /* Más grande que el normal */
  color: #2E7D32; /* Verde oscuro */
  margin-bottom: 10px;
}
#inicio-section p {
  font-family: 'Verdana', sans-serif;
  font-size: 18px;
  color: #1B5E20;
}

/* --- BARRA LATERAL --- */
/* =======================
   BARRA LATERAL
   ======================= */
nav {
  background-color: #79EB73; /* Verde de la barra */
  width: 120px; /* Hacer la barra un poco más ancha */
  height: 100vh; /* Que ocupe toda la altura de la pantalla */
  position: fixed;
  top: 0;
  left: 0;
  padding-top: 20px; /* Espacio superior */
  border-radius: 0 10px 10px 0; /* Bordes redondeados a la derecha */
  box-shadow: 3px 0 10px rgba(0,0,0,0.2); /* Sombra */
}

nav ul {
  list-style: none; /* Quitar viñetas */
  padding: 0;
  margin: 0;
}

nav li a {
  display: block;
  padding: 20px; /* Más espacio dentro del botón */
  color: white; 
  text-decoration: none;
  font-size: 18px; /* Fuente más grande */
  text-align: center;
  font-weight: bold; /* Letra más gruesa */
}

nav li a:hover {
  background: rgba(255,255,255,0.2); /* Efecto al pasar el ratón */
}

nav ul {
  list-style: none;
  padding: 0;
  margin: 0;
}
nav li a {
  display: block;
  padding: 10px;
  color: white;
  text-decoration: none;
  font-size: 12px;
  text-align: center;
}
nav li a:hover {
  background: rgba(255,255,255,0.2);
}

/* --- SECCIONES --- */
.contenido {
  display: none; /* Ocultamos todas las secciones al inicio */
  margin-left: 120px; /* Dejamos espacio para la barra lateral */
  padding: 20px;
}

/* Primera sección visible */
#inicio-section {
  display: block; /* Al cargar la página, se muestra la sección de inicio */
}

/* --- TRES COLUMNAS --- */
.contenedor {
  display: flex;
  gap: 20px; /* Separación entre columnas */
}
.columna {
  flex: 1;
  background: #94CF91;
  padding: 20px;
  border: 1px solid #ddd;
}
.columna h2 {
  border-bottom: 3px solid #79EB73; /* Línea verde para títulos */
  padding-bottom: 5px;
}

/* --- BANNER --- */
.banner img {
  width: 100%;
  height: auto;
  border-radius: 15px;
  margin-bottom: 20px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
}

/* --- PIE DE PÁGINA --- */
footer {
  background-color: #79EB73;
  color: white;
  text-align: center;
  padding: 15px;
  margin-top: 20px;
}

/* --- BOTÓN IR AL INICIO --- */
#btnInicio {
  position: fixed;
  bottom: 20px; /* Abajo a la derecha */
  right: 20px;
  padding: 10px 15px;
  background-color: #79EB73;
  color: white;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  box-shadow: 0 4px 6px rgba(0,0,0,0.2);
  font-size: 14px;
}
#btnInicio:hover {
  background-color: #4CAF50;
}

/* --- RESPONSIVE --- */
@media (max-width: 700px) {
  .contenedor {
    flex-direction: column;
  }
}
</style>
</head>
<body>

<!-- =======================
     BARRA LATERAL
     ======================= -->
<nav>
  <ul>
    <li><a href="#" onclick="mostrarSeccion('inicio-section')">Inicio</a></li>
    <li><a href="sobremi.html">Sobre mí</a></li>
    <li><a href="#" onclick="mostrarSeccion('contacto-section')">Contacto</a></li>
  </ul>
</nav>

<!-- =======================
     SECCIÓN INICIO
     ======================= -->
<div id="inicio-section" class="contenido" style="display:block;">

  <header>
    <h1>MI PRIMERA WEB</h1>
    <p>Soy Paula y estudio 2º de Bachillerato.</p>
  </header>

  <!-- Banner después de la presentación -->
  <div class="banner">
    <img src="banner4.jpg" alt="Banner principal">
  </div>

  <div class="contenedor">
    <div class="columna">
      <h2>Mis Hobbies</h2>
      <table border="1">
        <tr>
          <td><img src="https://www.andiar.com/3253-thickbox_default/vinilo-sinfonia-cascos.jpg" width="200"></td>
          <td><img src="https://www.shutterstock.com/image-photo/happy-mongrel-dog-puppy-smiling-600nw-2662330321.jpg" width="200"></td>
        </tr>
        <tr>
          <td><img src="https://www.informador.mx/__export/1706845619285/sites/elinformador/img/2024/02/01/conciertos_febrero_crop1706845617917.png_423682103.png" width="200"></td>
          <td><img src="https://cdn-images.dzcdn.net/images/cover/de5d0fde35ed4b805acb9e809a5b8ff2/500x500-000000-80-0-0.jpg" width="200"></td>
        </tr>
      </table>
    </div>

    <div class="columna">
      <h2>Enlaces a mis lugares favoritos</h2>
      <p>Aquí te muestro unos enlaces a mis lugares favoritos.</p>
      <ul>
        <li><a href="https://www.islacanela.es/que-hacer/playa-isla-canela">Playa Isla Canela</a></li>
        <li><a href="https://www.realbetisbalompie.es/club/estadio-benito-villamarin">Estadio Benito Villamarín</a></li>
        <li><a href="https://www.visitportugal.com/es/destinos/porto-e-norte/73739">Vila Real</a></li>
      </ul>
    </div>
  </div>
</div>

<!-- =======================
     SECCIÓN CONTACTO
     ======================= -->
<div id="contacto-section" class="contenido">
  <h2>Contacto</h2>
  <p>Rellena este formulario para contactar conmigo:</p>

  <!-- FORMULARIO DE GOOGLE FORMS -->
  <iframe src="https://docs.google.com/forms/d/e/1FAIpQLScJntN7aHK4rLLbJeq--NAlo75JdInqmOniuaEPBylzdqt6hg/viewform?embedded=true" 
          width="100%" height="800" 
          frameborder="0" marginheight="0" marginwidth="0">Cargando…</iframe>
</div>

<!-- =======================
     PIE DE PÁGINA
     ======================= -->
<footer>
  <p>© 2025 Mi sitio web | Todos los derechos reservados</p>
</footer>

<!-- =======================
     BOTÓN IR AL INICIO
     ======================= -->
<button id="btnInicio" onclick="window.scrollTo({ top: 0, behavior: 'smooth' });">↑ Inicio</button>

<script>
function mostrarSeccion(id) {
  document.querySelectorAll('.contenido').forEach(sec => sec.style.display = 'none');
  document.getElementById(id).style.display = 'block';
}
</script>

</body>
</html>

<script setup>
import NavBar from './components/NavBar.vue';
import DatosPersonales from './components/DatosPersonales.vue';
import Educacion from './components/EducacionComponente.vue';
import ExperienciaComponente from './components/ExperienciaComponente.vue';
import ProyectosComponentes from './components/ProyectosComponentes.vue';
import HabilidadesComponentes from './components/HabilidadesComponentes.vue';
import InteresesComponente from './components/InteresesComponentes.vue';

</script>

<template>
  <header id="footer">
    <!--Barra de navegacion-->
    <NavBar />
    <!--Datos Personales-->
    <DatosPersonales />
    
    
       

  </header>
  <main>
    <!-- el estilo de section se encuentra en base.css-->
    <section id="educacion"><h2>Educacion - Cursos </h2></section>
    <Educacion />
    <section id="experiencia"><h2>Experiencia</h2></section>
    <ExperienciaComponente />
    <section id="proyectos"><h2>Proyectos </h2></section>
    <ProyectosComponentes />
    <section id="habilidades"><h2>Habilidades</h2></section>
    <HabilidadesComponentes />
    <section id="intereses"><h2>Intereses</h2></section>
    <InteresesComponente />
    
    
    
  </main>
<footer class="footer">
  <li> <a href="#footer">Inicio</a></li>
    <p>© 2025 Oscar Mendez- Portafolio-web</p>
  
     <li> <a href="https://github.com/OskyMendez" target="_blank">GitHub</a></li>
  
  </footer>

  
  
</template>

<style scoped>
section {
  margin: 3rem 0;
  padding-bottom: 1rem;
  border-bottom: 2px solid rgba(7, 7, 7, 0.2); /* línea blanca moderna */
}

section h2 {
  text-align: center;
  font-weight: bold;
  font-size: 1.8rem;
  color: #050505;
  margin-bottom: 1rem;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.6);
}

h2 {
  font-size: 2rem; /* más grande */
  font-weight: bold;
  text-align: center;
  background: #838383; /* ← gris sólido */
  color: #050505;
  padding: 1rem;
  border-radius: 8px;
  margin-bottom: 1.5rem;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
  text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.6);
}

.footer {
  color: #f0f6fc;
  text-align: center;
  padding: 2rem 1rem;
  font-size: 1rem;
  font-weight: 500;
  animation: fadeInUp 1s ease forwards;
  opacity: 0;
}

.footer a {
  display: inline-block;
  margin-top: 0.5rem;
  color: #58a6ff;
  text-decoration: none;
  font-weight: bold;
  transition: color 0.3s ease;
}

.footer a:hover {
  color: #fbf9f9;
}


</style>


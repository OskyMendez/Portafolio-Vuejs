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
  <header>
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
  
  
</template>

<style scoped>


section {
  margin: 3rem 0;
  padding-bottom: 1rem;
  border-bottom: 2px solid rgba(255, 255, 255, 0.2); /* línea blanca moderna */
}

section h2 {
  text-align: center;
  font-weight: bold;
  font-size: 1.8rem;
  color: #f0f6fc;
  margin-bottom: 1rem;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.6);
}
h2 {
  font-size: 2rem; /* más grande */
  font-weight: bold;
  text-align: center;
  background: linear-gradient(135deg, #2c3e50, #000000); /* fondo azul degradado */
  color: #f0f6fc;
  padding: 1rem;
  border-radius: 8px;
  margin-bottom: 1.5rem;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
  text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.6);
}


</style>

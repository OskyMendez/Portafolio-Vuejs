<script setup>
import { ref } from 'vue'

const mostrarExtra = ref(false)
</script>

<template>
  <section>
    <h2>Experiencia</h2>

    <div class="parrafo-box">
      <p>Actualmente no cuento con experiencia formal en el área, ya que estoy finalizando el primer año de la Tecnicatura en Programación.</p>
    </div>

    <div class="parrafo-box">
      <p>En este tiempo he participado en proyectos grupales junto a mis compañeros, resolviendo desafíos técnicos y colaborativos para distintos trabajos académicos.</p>
    </div>

    <div class="parrafo-box">
      <p>Creé mi perfil de GitHub donde subo mis proyectos personales y grupales, como muestra de mi evolución y compromiso con el aprendizaje.</p>
    </div>

 

    <button @click="mostrarExtra = !mostrarExtra">
      {{ mostrarExtra ? 'Ocultar detalle' : 'Ver más' }}
      
    </button>
     

    <div v-if="mostrarExtra" class="parrafo-box">
      <img src="/github.png" alt="GitHub" />
      <a href="https://github.com/OskyMendez" target="_blank">Enlace a mi GitHub</a>
    </div>
  </section>
</template>
<style scoped>
section {
  background-color: #2c3e50; /* Azul oscuro */
  border: 2px solid #ffffff;
  border-radius: 16px;
  padding: 2rem;
  max-width: 800px;
  margin: 2rem auto;
  box-shadow: 0 6px 16px rgba(0, 0, 0, 0.1);
  color: #ffffff;
  font-family: 'Segoe UI', sans-serif;
  text-align: center;
}

/* Título con subrayado y fuente especial */
h2 {
  font-size: 2.2rem;
  margin-bottom: 1.5rem;
  color: #ffffff;
  font-family: 'Montserrat', sans-serif;
  text-decoration: underline;
  text-underline-offset: 6px;
}

/* Contenedor para cada párrafo */
.parrafo-box {
  background-color: #3b4d61; /* Azul más claro para destacar */
  border-radius: 12px;
  padding: 1rem 1.5rem;
  margin-bottom: 1rem;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  text-align: left;
}

/* Texto dentro del box */
.parrafo-box p {
  font-size: 1rem;
  line-height: 1.6;
  margin: 0;
  color: #ffffff;
}

/* Enlace GitHub */
a {
  color: #0c0c0c;
  font-weight: bold;
  text-decoration: underline;
}

a:hover {
  color: #e0e0e0;
}

/* Ícono GitHub */
img {
  width: 24px;
  height: 24px;
  vertical-align: middle;
}

/* Contenedor del enlace */
div {
  justify-content: center;
  margin-top: 1rem;
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

button {
  margin-top: 1rem;
  padding: 0.5rem 1rem;
  font-size: 1rem;
  background-color: #0c0c0c;
  color: white;
  border: none;
  border-radius: 8px;
  cursor: pointer;
}

button:hover {
  background-color: #3b4d61;
}
</style>

<script setup>
import { ref } from 'vue'

const mostrarExtra = ref(false)
</script>

<template>
  <div class="experiencia">
    <h2 class="titulo-seccion">Experiencia Profesional</h2>

    <div class="experiencia-item">
      <h3>MORDIDITAS PET SHOP</h3>
      <span class="fecha">Año 2024</span>
      <p>Trabajé en la creación de la página web para la pyme Pet Shop Mordiditas, desarrollando una plataforma de comercio electrónico que impulsó sus ventas.</p>
    </div>

    <div class="experiencia-item">
      <h3>SISTEMA HOSPITALARIO - CIRUGÍA CARDIOVASCULAR</h3>
      <span class="fecha">Año 2025</span>
      <p>Participé en el desarrollo del sistema hospitalario para el Servicio de Cirugía Cardiovascular y Trasplante del Hospital Italiano de Mendoza, integrando soluciones digitales para mejorar la gestión médica.</p>
    </div>

    <div class="experiencia-item">
      <h3>MIGUEL STENT - SISTEMA DE VENTAS Y CONTROL</h3>
      <span class="fecha">Año 2025 (actual)</span>
      <p>Actualmente estoy trabajando en el desarrollo de un sistema de ventas y control de stock para la pyme Miguel Stent, enfocado en la trazabilidad de stents cardiovasculares e integración comercial.</p>
    </div>
  </div>
</template>

<style scoped>
.experiencia {
  width: 100%;
  max-width: 1000px;
  margin: 0 auto;
  padding: 60px 20px;
  display: flex;
  flex-direction: column;
  gap: 30px;

  border-radius: 16px;
  box-shadow: 0 8px 24px rgba(247, 246, 246, 0.3);
}


.titulo-seccion {
  font-size: 2rem;
  font-weight: 800;
  text-align: center;
  color: #ffffff;
  text-transform: uppercase;
  letter-spacing: 1.5px;
  margin-bottom: 20px;
  border-bottom: 2px solid #ffffff;
  padding-bottom: 10px;
}

.experiencia-item {
  background-color: #838383 ;
  border: 1px solid rgba(255, 255, 255, 0.1); /* borde sutil */
  border-radius: 16px; /* esquinas redondeadas */
  padding: 20px;

  box-shadow: 0 8px 24px rgba(15, 15, 15, 0.3); /* sombra elegante */
  backdrop-filter: blur(6px); /* efecto glassmorphism */
  transition: transform 0.3s ease, box-shadow 0.3s ease, border 0.3s ease;
  position: relative;
  overflow: hidden;
}

/* Efecto al pasar el mouse */
.experiencia-item:hover {
  transform: translateY(-5px);
  box-shadow: 0 12px 32px rgba(14, 14, 14, 0.3);
  border: 1px solid rgba(13, 13, 14, 0.3); /* borde con brillo azul */
}

/* Detalle decorativo opcional */
.experiencia-item::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 4px;
  background: linear-gradient(to right, #131313, #060606);
  opacity: 0.6;
}

.experiencia-item h3 {
  font-size: 1.4rem;
  font-weight: 700;
  margin-bottom: 8px;
  color: #0a0a0a;
  text-transform: uppercase;
}

.fecha {
  font-size: 0.9rem;
  color: #030303;
  margin-bottom: 12px;
  display: block;
}

.experiencia-item p {
  font-size: 1rem;
  line-height: 1.5;
  color: #0c0c0c;
}

/* Fondo animado */
@keyframes galeriaGradient {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}

/* Responsive */
@media (max-width: 768px) {
  .experiencia {
    padding: 40px 15px;
  }

  .titulo-seccion {
    font-size: 1.6rem;
  }

  .experiencia-item h3 {
    font-size: 1.2rem;
  }

  .experiencia-item p {
    font-size: 0.95rem;
  }
}

</style>

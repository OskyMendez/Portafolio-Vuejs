<script setup>
import imagen1 from '/src/assets/pet-shop.jpg'
import imagen2 from '/src/assets/cirugia-cardiovascular.jpg'
import imagen3 from '/src/assets/miguel.jpg'
const proyectos = [
  {
    id: 1,
    titulo: "MORDIDITAS PET SHOP",
    descripcion:
      "Desarrollé la plataforma web de comercio electrónico para el Pet Shop Mordiditas, logrando un incremento del 30% en sus ventas durante el primer año.",
    imagen: imagen1,
    enlaceProyecto: "",
    enlaceGithub: "https://github.com/OskyMendez",
  },
  {
    id: 2,
    titulo: "SISTEMA HOSPITALARIO - CIRUGÍA CARDIOVASCULAR",
    descripcion:
      "Formé parte del equipo que desarrolló el sistema hospitalario del Servicio de Cirugía Cardiovascular y de Trasplante del Hospital Italiano de Mendoza, integrando soluciones digitales para optimizar procesos médicos y administrativos.",
    imagen: imagen2,
    enlaceProyecto: "http://168.227.97.240/pages-login.php",
    enlaceGithub: "https://github.com/OskyMendez",
  },
  {
    id: 3,
    titulo: "CONTROL DE STOCK - MIGUEL STENT",
    descripcion:
      "En proceso de creación de un sistema integral para la gestión de ventas de stents cardiovasculares, adaptado a las necesidades operativas de la pyme Miguel Stent. Incluye módulos de inventario, trazabilidad por lote, registro de clientes y visualización dinámica de movimientos comerciales.",
    imagen: imagen3,
    enlaceProyecto: "",
    enlaceGithub: "https://github.com/OskyMendez",
  },
];


</script>
<template>
  <div class="galeria">
    <div class="proyecto" v-for="proyecto in proyectos" :key="proyecto.id">
      <img :src="proyecto.imagen" :alt="`Proyecto ${proyecto.titulo}`" />
      <div class="proyecto-info">
        <h3>{{ proyecto.titulo }}</h3>
        <p>{{ proyecto.descripcion }}</p>
        <div class="proyecto-links">
          <a :href="proyecto.enlaceProyecto" class="btn-ver-mas" target="_blank" rel="noopener noreferrer">
            Ver Proyecto
          </a>
          <a :href="proyecto.enlaceGithub" class="github-link" target="_blank" rel="noopener noreferrer">
            Ver código en GitHub
          </a>
        </div>
      </div>
    </div>
  </div>
</template>



<style scoped>
/* .galeria{
    width: 100%;
    height: 100vh;
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
    background-image: url('/src/assets/fondo-proyectos.jpg');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
} */
.galeria {
  width: 100%;
  min-height: 100vh;
  display: flex;
  flex-wrap: wrap;
  gap: 30px;
  padding: 40px;
  justify-content: center;
  background:  #838383;

  background-size: 400% 400%;
  animation: galeriaGradient 20s ease infinite;
}

/* Animación suave del fondo */
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

/* Tarjeta de proyecto */
.proyecto {
  display: flex;
  flex-direction: column;
  border: 2px solid transparent;
  border-radius: 12px;
  overflow: hidden;
  position: relative;
  width: 340px;
  height: auto;
  flex-shrink: 0;
  animation: fadeUp 0.8s ease forwards;
  opacity: 0;
  background: #2c2c2c; /* gris más oscuro */
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}



.proyecto:hover {
  transform: translateY(-5px);
}

.proyecto img {
  width: 100%;
  height: auto;
  display: block;
}

.proyecto-info {
  padding: 20px;
  text-align: center;
}

.proyecto-info h3 {
  margin: 10px 0;
  font-size: 1.6rem;
  font-weight: 700;
  color: #fcfdfd;
  text-transform: uppercase;
  letter-spacing: 1px;
  border-bottom: 2px solid #f6f6f7;
  padding-bottom: 5px;
}

.proyecto-info p {
  margin: 10px 0;
  font-size: 1em;
  color: #faf9f9;
}

.proyecto-links {
  display: flex;
  flex-direction: column;
  gap: 10px;
  margin-top: 15px;
}

.btn-ver-mas,
.github-link {
  display: inline-block;
  padding: 10px 15px;
  font-size: 0.95rem;
  font-weight: bold;
  text-align: center;
  text-decoration: none;
  border-radius: 6px;
  transition: background-color 0.3s ease, transform 0.2s ease;
  color: #ffffff;
  background-color: #010101;
  border: none;
}

.btn-ver-mas:hover,
.github-link:hover {
  background-color: #0e0e0e;
  transform: scale(1.05);
}

/* 📱 Adaptación para celulares */
@media (max-width: 768px) {
  .galeria {
    flex-direction: column;
    align-items: center;
    padding: 20px;
  }

  .proyecto {
    width: 100%;
    max-width: 90%;
  }
}
/* Animación base */
@keyframes fadeUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Aplicar a cada tarjeta */
.proyecto {
  animation: fadeUp 0.8s ease forwards;
  opacity: 0;
}
.proyecto {
  animation: fadeUp 0.8s ease forwards;
  opacity: 0;}

.proyecto::before {
  content: "";
  position: absolute;
  inset: 0;
  border-radius: 12px;
  padding: 2px;
  background: linear-gradient(135deg, #ffffff, #e8eaeb);
  -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
  -webkit-mask-composite: destination-out;
  mask-composite: exclude;
  pointer-events: none;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.proyecto:hover::before {
  opacity: 1;
}

.proyecto:hover {
  transform: scale(1.03);
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.3);
}
@keyframes gradientShift {
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



/* Delay escalonado para cada tarjeta */
.proyecto:nth-child(1) { animation-delay: 0.2s; }
.proyecto:nth-child(2) { animation-delay: 0.4s; }
.proyecto:nth-child(3) { animation-delay: 0.6s; }




</style>
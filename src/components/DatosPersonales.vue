<script setup>
const title= "Oscar Mendez";
const descripcion="Estudiante de la Tecnicatura Universitaria en Programacion";
const presentacion1="Soy Oscar Méndez, Técnico Superior en Anestesiología con amplia experiencia en el ámbito hospitalario.";
const presentacion2="Actualmente me encuentro cursando el primer año de la carrera universitaria en Programación, combinando mi formación en salud con el desarrollo de soluciones tecnológicas. Este espacio refleja mi transición profesional, mi compromiso con el aprendizaje continuo y mi pasión por crear proyectos funcionales, modernos y alineados con buenas prácticas";
const residencia="Guaymallen- Mendoza";
const redesSociales=[
    {id: 1, name: 'Instagram', src: '/instagram.png', url: 'https://www.instagram.com/oskymendezoldra' },
    {id: 2, name: 'GitHub', src: '/github.png', url: 'https://github.com/OskyMendez'},
    {id: 3, name: 'Linkedin', src: '/linke.png', url: 'https://www.linkedin.com/in/oscar-mendez-278b13315/'},
    
]
const telefono= "Mi telefono personal: 2622575468";
</script>

<template>
<section class="Datos Personales">
 <div class="card">
    <h1> {{ title }}</h1>
    <h2>{{ descripcion }}</h2>
    <p>{{ presentacion1 }}</p>
    <p>{{ presentacion2 }}</p>
 <ul class="container-lista">
   <li v-for="red in redesSociales" :key="red.id">
    <a :href="red.url"><img class="icon-redsocial" :src="red.src" width="35rem" :alt="red.name"></a>
    </li>
</ul>
    <h3> {{ telefono }}</h3>
    <h4>{{ residencia }}</h4>
</div>
</section>
</template>
<style scoped>
/* Fondo general */
section.Datos.Personales {
  background: linear-gradient(to right, var( --vt-c-indigo) , hsla(180, 82%, 40%, 0.2););
  padding: 2rem;
  display: flex;
  justify-content: center;
  font-family: 'Segoe UI', sans-serif;
}

/* Tarjeta principal */
.card {
  background-color: #2c3e50 ;
  border-radius: 12px;
  box-shadow: 0 4px 12px rgb(245, 240, 240);
  padding: 2rem;
  max-width: 600px;
  width: 100%;
  color: #f5f8fa;
}

/* Títulos */
.card h1 {
  font-size: 3rem; /* Mucho más grande */
  font-weight: 700; /* Negrita fuerte */
  color: #f6f8fb; /* Azul oscuro elegante */
  text-align: center;
  margin-bottom: 1rem;
  letter-spacing: 1px;
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.1); /* Sombra suave para resaltar */
  border-bottom: 2px solid #f6f9fd; /* Línea azul moderna debajo */
  padding-bottom: 0.5rem;
}


.card h2 {
  font-size: 1.2rem;
  color: #ffffff;
  margin-bottom: 0.5rem;
}

.card h3 {
  font-size: 1rem;
  color: #f6f7f8;
  margin-top: 1.5rem;
}

.card h4 {
  font-size: 0.9rem;
  color: #fbfcfe;
}

/* Párrafos */
.card p {
  font-size: 1rem;
  line-height: 1.6;
  color: #f1f2f3;
  margin-bottom: 1rem;
}

/* Lista de redes sociales */
.container-lista {
  display: flex;
  gap: 1rem;
  list-style: none;
  padding: 0;
  margin-top: 1rem;
  justify-content: center;
}

.icon-redsocial {
  transition: transform 0.3s ease, filter 0.3s ease;
  border-radius: 50%;
  background-color: #e2e8f0;
  padding: 0.3rem;
}

.icon-redsocial:hover {
  transform: scale(1.1);
  filter: brightness(1.2);
}

</style>
<script setup>
const skills = [
  {
    categoria: 'Lenguajes de Programación',
    items: [
      { nombre: 'JavaScript', nivel: 'Intermedio', icono: '/public/javascript.svg' },
      { nombre: 'Python', nivel: 'Intermedio', icono: '/public/python.svg' },
      { nombre: 'HTML/CSS', nivel: 'Intermedio', icono: '/public/html.svg' },
      { nombre: 'Java', nivel: 'Intermedio', icono: '/public/java.svg' },
      { nombre: 'SQL', nivel: 'Intermedio', icono: '/public/sql.svg' },
    ],
  },
  {
    categoria: 'Frameworks y Librerías',
    items: [
      { nombre: 'React.js', nivel: 'Intermedio', icono: '/public/react.svg' },
      { nombre: 'Vue.js', nivel: 'Intermedio', icono: '/public/vue.svg' },
      { nombre: 'Node.js', nivel: 'Intermedio', icono: '/public/node.svg' },
      { nombre: 'Django', nivel: 'Intermedio', icono: '/public/django.svg' },
      { nombre: 'Bootstrap', nivel: 'Intermedio', icono: '/public/bootstrap.svg' },
    ],
  },
  {
    categoria: 'Herramientas y Software',
    items: [
      { nombre: 'Git', nivel: 'Avanzado', icono: '/public/git.svg' },
      { nombre: 'Docker', nivel: 'Intermedio', icono: '/public/docker.svg' },
      { nombre: 'Cypress', nivel: 'Intermedio', icono: '/public/Cypress.svg' },
      { nombre: 'Figma', nivel: 'Intermedio', icono: '/public/figma.svg' },
      { nombre: 'Visual Studio Code', nivel: 'Avanzado', icono: '/public/visual.svg' },
    ],
  },
  {
    categoria: 'Bases de Datos',
    items: [
      { nombre: 'MongoDB', nivel: 'Avanzado', icono: '/public/mongo.svg' },
      { nombre: 'MySQL', nivel: 'Intermedio', icono: '/public/sql.svg' },
      { nombre: 'PostgreSQL', nivel: 'Intermedio', icono: '/public/postgresql.svg' },
    ],
  },
  {
    categoria: 'Idiomas',
    items: [
      { nombre: 'Español', nivel: 'Nativo', icono: '/public/spanish.svg' },
      { nombre: 'Inglés', nivel: 'Intermedio', icono: '/public/inglish.svg' },
    ],
  },
]
</script>

<template>
  <div v-for="(grupo, index) in skills" :key="index" class="skills-contenedor">
    <h3>{{ grupo.categoria }}</h3>
    <ul class="skills-categoria">
      <li v-for="(item, i) in grupo.items" :key="i" class="skill">
        <img :src="item.icono" :alt="item.nombre" />
        <span>{{ item.nombre }}</span>
        <span class="nivel">{{ item.nivel }}</span>
      </li>
    </ul>
  </div>
</template>


<style scoped>

.skills-contenedor {
  margin: 2rem auto;
  padding: 1rem;
  border-bottom: 1px solid #ccc;
  max-width: 900px; /* Limita el ancho para que no se desparrame */
  text-align: center;
  background-color: #090909 ;
}

.skills-contenedor h3 {
  font-size: 1.4rem;
  font-weight: 600;
  margin-bottom: 1rem;
  color: #f0f1f3;
  border-left: 4px solid #f6f8f9;
  padding-left: 0.5rem;
  display: inline-block;
  text-align: left;
}

.skills-categoria {
  list-style: none;
  padding: 0;
  display: flex;
  flex-wrap: wrap;
  justify-content: center; /* Centra las tarjetas */
  gap: 1rem;
}

.skill {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 120px;
  text-align: center;
  background-color: #2c5364;
  border-radius: 8px;
  padding: 0.8rem;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
}

.skill img {
  width: 40px;
  height: 40px;
  object-fit: cover;
  margin-bottom: 0.5rem;
  border-radius: 50%; /* Hace el ícono circular */
  border: 1px solid #f0f0f0;
}

.skill span {
  font-size: 0.9rem;
  color: #faf8f8;
}
.skill {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 120px;
  text-align: center;
  background-color: #2c5364;
  border-radius: 8px;
  padding: 0.8rem;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.skill:hover {
  transform: scale(1.08);
  box-shadow: 0 4px 12px rgba(255, 255, 255, 0.2);
}

</style>
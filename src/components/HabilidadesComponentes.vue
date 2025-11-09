<script setup>
import javascript from '/public/javascript.svg'
import python from '/public/python.svg'
import html from '/public/html.svg'
import java from '/public/java.svg'
import sql from '/public/sql.svg'
import react from '/public/react.svg'
import vue from '/public/vue.svg'
import node from '/public/node.svg'
import django from '/public/django.svg'
import bootstrap from '/public/bootstrap.svg'
import git from '/public/git.svg'
import docker from '/public/docker.svg'
import Cypress from '/public/Cypress.svg'
import figma from '/public/figma.svg'
import visualcode from  '/public/visual.svg'
import mongo from '/public/mongo.svg'
import mysql from '/public/sql.svg'
import postgre from '/public/postgresql.svg'
import español from '/public/spanish.svg'
import ingles from '/public/inglish.svg'



const skills = [
  {
    categoria: 'Lenguajes de Programación',
    items: [
      { nombre: 'JavaScript', nivel: 'Intermedio', icono: javascript },
      { nombre: 'Python', nivel: 'Intermedio', icono: python },
      { nombre: 'HTML/CSS', nivel: 'Intermedio', icono: html },
      { nombre: 'Java', nivel: 'Intermedio', icono: java },
      { nombre: 'SQL', nivel: 'Intermedio', icono: sql },
    ],
  },
  {
    categoria: 'Frameworks y Librerías',
    items: [
      { nombre: 'React.js', nivel: 'Intermedio', icono: react },
      { nombre: 'Vue.js', nivel: 'Intermedio', icono: vue},
      { nombre: 'Node.js', nivel: 'Intermedio', icono: node },
      { nombre: 'Django', nivel: 'Intermedio', icono: django },
      { nombre: 'Bootstrap', nivel: 'Intermedio', icono: bootstrap },
    ],
  },
  {
    categoria: 'Herramientas y Software',
    items: [
      { nombre: 'Git', nivel: 'Avanzado', icono: git },
      { nombre: 'Docker', nivel: 'Intermedio', icono: docker },
      { nombre: 'Cypress', nivel: 'Intermedio', icono: Cypress},
      { nombre: 'Figma', nivel: 'Intermedio', icono: figma },
      { nombre: 'Visual Studio Code', nivel: 'Avanzado', icono: visualcode},
    ],
  },
  {
    categoria: 'Bases de Datos',
    items: [
      { nombre: 'MongoDB', nivel: 'Avanzado', icono: mongo },
      { nombre: 'MySQL', nivel: 'Intermedio', icono: mysql },
      { nombre: 'PostgreSQL', nivel: 'Intermedio', icono: postgre },
    ],
  },
  {
    categoria: 'Idiomas',
    items: [
      { nombre: 'Español', nivel: 'Nativo', icono: español },
      { nombre: 'Inglés', nivel: 'Intermedio', icono: ingles },
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
  background-color: #838383;
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
  color: #060606;
}
.skill {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 120px;
  text-align: center;
  background-color: #838383;
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
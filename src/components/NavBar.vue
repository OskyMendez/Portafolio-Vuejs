<template>
    <nav class="navbar">
      <div class="navbar-menu">
        <ul>
          <a v-for="nav in navegacion" :key="nav.nombre" :href="nav.enlace" class="navbar-item" > {{ nav.nombre }}</a>
        </ul>
      </div>
    </nav>
</template>
<script setup>
import { ref } from 'vue';
const navegacion= ref([
    {id:1, nombre: 'Educacion', enlace: '#educacion'},
    {id:2, nombre: 'Experiencia', enlace: '#experiencia'},
    {id:3, nombre: 'Proyectos', enlace: '#proyectos'},
    {id:4, nombre: 'Habilidades', enlace: '#habilidades'},
    {id:5, nombre: 'Intereses', enlace: '#intereses'},
   
])

</script>
<style scoped>
.navbar {
  position: sticky;
  top: 0;
  z-index: 1000;

  background-color: #0f0f0f;
  color: #ffffff;
  padding: 0.75rem 1.5rem;
  display: flex;
  align-items: center;
  justify-content: space-between;

  border-bottom: 1px solid rgba(255, 255, 255, 0.1);
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.4);
  backdrop-filter: blur(6px);
}



.navbar-item {
  text-decoration: none;
  margin-right: 1rem;
  color: #f9f8f8;

}
.navbar-menu{
  display: flex;
  justify-content: flex-end;
}
.nav-list {
  list-style: none;
}
a{
    border: 1px solid;
    border-color: hsla(0, 0%, 100%, 0.2);
    border-radius: 5px;
    /*Elimina la subrayada de los enlaces y elementos con clase "green" */
    text-decoration: none;
    /*Añade padding alrededor del contenido */
    padding: 5px;
}
a:hover{
    /*Cambia el color de fondo al pasasr el mouse sobre el enlace*/
    background-color: rgba(200, 200, 200, 0.2);

}
@media(max-width: 768px) {
    .navbar-menu {
        display: flex;
        justify-content: flex-end;
        width: 100%;
    }
}


</style>
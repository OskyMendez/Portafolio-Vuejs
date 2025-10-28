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
    {id:3, nombre: 'Proyectos', enlace: '#proyecto'},
    {id:4, nombre: 'Habilidades', enlace: '#habilidades'},
    {id:5, nombre: 'Intereses', enlace: '#intereses'},
   
])

</script>
<style scoped>
.navbar {
  background-color: var( --vt-c-indigo);
  color: #e6e3f1;
  padding: 0.5rem 1rem;
  align-items: center;
}
.navbar-item {
  text-decoration: none;
  margin-right: 1rem;
  color: #f2e3e3;

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
    border-color: hsla(0, 100%, 0%, 0.2);
    border-radius: 5px;
    /*Elimina la subrayada de los enlaces y elementos con clase "green" */
    text-decoration: none;
    /*Añade padding alrededor del contenido */
    padding: 5px;
}
a:hover{
    /*Cambia el color de fondo al pasasr el mouse sobre el enlace*/
    background-color: hsla(180, 82%, 40%, 0.2);
}
@media(max-width: 768px) {
    .navbar-menu {
        display: flex;
        justify-content: flex-end;
        width: 100%;
    }
}


</style>
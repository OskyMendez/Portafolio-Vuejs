<script setup>
</script>
<template>
  <div class="galeria">
    <div class="proyecto">
      <img src="" alt="Proyecto 1" />
      
      <div class="proyecto-info">
        <h3>Ecommerce</h3>
        <p>Creé una plataforma de comercio electrónico que incrementó un 30% las ventas el primer año.</p>
        
        <div class="proyecto-links">
          <a href="" class="btn-ver-mas" target="_blank" rel="noopener noreferrer">
            Ver Proyecto
          </a>
          <a href="" class="github-link" target="_blank" rel="noopener noreferrer">
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
 .galeria{
    
    width: 100%;
    height: 100%;
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    padding: 20px;
    justify-content: center;
    background: linear-gradient(-45deg, #021526, #2c3e50 , #6EACDA,#E2E286);
    background-size: 400% 400%;
    animation: gradient 15s ease infinite;
 }
 @keyframes gradient{
    0% {
        background: 0% 50%;
    }
    50%{
        background-position: 100% 50%;
        
    }
    100%{
        background-position: 0% 50%;
    }

 }
 .proyecto{
    display: flex;
    flex-direction: column;
    border: 2px solid #ddd;
    border-radius: 8px;
    overflow: hidden;
    background-color: #f9f9f9;
    max-width: 222px;
    flex: 1 1 300px;

 }
 .proyecto img{
    width: 100%;
    height: auto;
    display: block;
 }
 .proyecto-info {
    padding: 15px;
    text-align: center;
 }
 .proyecto-info h3{
    margin: 10px;
    font-size: 1.3rem;
    color: #333
 }
 .proyecto-info p{
    margin: 10px 0;
    font-size: 1em;
    color:#666;
 }
 .proyecto-links{
    display: flex;
    flex-direction: column;
    gap: 10px;
    margin-top: 10px;
 }
</style>
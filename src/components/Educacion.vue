
<script setup>
const experiencias = [
  {
    fecha: '2011',
    titulo: 'Finalización del Secundario',
    descripcion: 'Finalización de estudios secundarios en la Escuela 9-004 "Normal General Superior Toribio de Luzuriaga"',
  },
  {
    fecha: '2012–2015',
    titulo: 'Técnico Superior en Anestesiología',
    descripcion: 'Egresado del Instituto de Ciencias Biomédicas "San Agustín"',
  },
  {
    fecha: '2024–Actualidad',
    titulo: 'Tecnicatura en Programación',
    descripcion: 'Actualmente cursando el segundo año en la Tecnicatura Universitaria en Programación',
  },
]
</script>




    <template>
  <div class="timeline">
    <div class="outer">
      <div class="card" v-for="(exp, index) in experiencias" :key="index">
        <div class="info">
          <span class="fecha">{{ exp.fecha }}</span>
          <h3 class="title">{{ exp.titulo }}</h3>
          <p>{{ exp.descripcion }}</p>
        </div>
      </div>
    </div>
  </div>


    <!--
    <div class="timeline">
  <div class="outer">
    <div class="card">
      <div class="info">
        <span class="fecha">2011</span>
        <h3 class="title">Finalizacion del Secundario</h3>
        <p>Finalizacion de estudios secunadrio en la Escuela   9-004 "Normal General Superior Toribio de Luzuriaga"</p>
      </div>
    </div>
    <div class="card">
      <div class="info">
        <span class="fecha">2012-2015</span>
        <h3 class="title">Tecnico Superior en Anestesiologia</h3>
        <p>Egresado del Instituto de Ciencias Biomedicas "San Agustin"</p>
      </div>
    </div>
    <div class="card">
      <div class="info">
        <span class="fecha">2024-Actualidad</span>
        <h3 class="title">Tecnicatura en Programacion</h3>
        <p>Actualmente cursando el segundo año en la Tecnicatura Universitario en Programacion </p>
      </div>
    </div>
    
    
      
    
  </div>
</div>
-->

</template>
<style scoped>
:root {
  --primary-color: #2c3e50;
  --background-color: #2c3e50;
  --font: sans-serif;
  --card-bg: #2c3e50;
  --card-shadow: rgba(0, 0, 0, 0.4);
}

body {
  background: var(--background-color);
  font-family: var(--font);
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}

/* Contenedor general centrado */
.timeline-wrapper {
  background-color: var(--card-bg);
  padding: 30px;
  border-radius: 20px;
  box-shadow: 0 0 20px var(--card-shadow);
  max-width: 900px;
  width: 100%;
  display: flex;
  justify-content: center;
}

/* Timeline */
.timeline {
  background: var(--primary-color);
  padding: 20px;
  border-radius: 12px;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

/* Tarjetas */
.card {
  position: relative;
  max-width: 600px;
  width: 100%;
  margin: 20px 0;
  padding: 30px;
  box-shadow: 0 0 12px rgba(255, 255, 255, 0.6); /* contorno blanco brillante */
  border-radius: 12px; /* opcional para suavizar bordes */
}


/* Línea lateral */
.card::before {
  content: "";
  position: absolute;
  top: 0;
  bottom: 0;
  width: 4px;
  background-color: #2c3e50;
  left: -20px;
  border-radius: 10px;
}

/* Contenido de cada tarjeta */
.info {
  background: #2c3e50 ;
  color: rgb(245, 244, 244);
  border-radius: 10px;
  padding: 20px;
  box-shadow: 0 0 10px rgba(255, 255, 255, 0.1);
}
.fecha{
     color: #ffffff;
  font-size: 1rem;
  font-weight: bold;
  text-shadow: 0 0 8px rgba(255, 255, 255, 0.6);
  position: relative;
  margin-bottom: 05px;

}

/* Títulos más blancos y brillantes */
.title {
  color: #f0f0f0; /* blanco más suave */
  font-size: 1.6rem;
  font-weight: bold;
  position: relative;
  margin-bottom: 10px;
  text-shadow: none; /* se elimina el brillo */
}

/* Punto decorativo */
.title::before {
  content: "";
  position: absolute;
  width: 12px;
  height: 12px;
  background: #2c3e50;
  border-radius: 50%;
  border: 3px solid #ffffff;
  left: -30px;
  top: 50%;
  transform: translateY(-50%);
  box-shadow: none; /* se elimina el brillo del punto */
}
</style>
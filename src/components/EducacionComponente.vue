
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
body {
  background: #d3d3d3; /* gris claro */
  font-family: sans-serif;
  display: flex;
  justify-content: center;   /* centra horizontal */
  align-items: center;       /* centra vertical */
  min-height: 100vh;         /* ocupa toda la pantalla */
}

/* Contenedor general */
.container {
  display: flex;
  flex-direction: column;    /* organiza las cards en columna */
  align-items: center;       /* centra horizontalmente */
  justify-content: center;   /* centra verticalmente */
  width: 100%;
  text-align: center;        /* centra texto dentro */
}

/* Tarjetas */
.card {
  position: relative;
  max-width: 600px;
  width: 100%;
  margin: 20px auto;         /* auto centra horizontalmente */
  padding: 50px;
  box-shadow: 0 0 12px rgba(7, 7, 7, 0.6);
  border-radius: 11px;
}

/* Línea lateral */
.card::before {
  content: "";
  position: absolute;
  top: 0;
  bottom: 0;
  width: 4px;
  background-color: #000000;
  left: 0;                   /* corregido: antes estaba -20px */
  border-radius: 10px;
}

/* Contenido de cada tarjeta */
.info {
  background: #838383;
  color: #0a0a0a;
  border-radius: 20px;
  padding: 25px;
  box-shadow: 0 0 10px rgba(255, 255, 255, 0.1);
  border: 2px solid #000000; /* contorno negro */
}


.fecha {
  color: #030303;
  font-size: 1rem;
  font-weight: bold;
  margin-bottom: 5px;
}

/* Títulos */
.title {
  color: #000000;
  font-size: rem;
  font-weight: bold;
  margin-bottom: 10px;
  position: relative;        /* necesario para el punto decorativo */
}

/* Punto decorativo */
.title::before {
  content: "";
  position: absolute;
  width: 12px;
  height: 12px;
  background: #000000;
  border-radius: 50%;
  border: 3px solid #ffffff;
  left: -30px;
  top: 50%;
  transform: translateY(-50%);
}
</style>



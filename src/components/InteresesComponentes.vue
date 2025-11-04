<script setup>
</script>

<template>
  <div class="intereses-contenedor">
    <ul class="contenedor-lista">
      <li class="item">
        Me destaco por mi capacidad para trabajar en equipo y colaborar en entornos multidisciplinarios.
        Me interesan profundamente los sistemas de software vinculados al área de salud, ya que desde hace años desarrollo mi carrera profesional en ese ámbito.
      </li>
      <li class="item">
        La música es la base de mis pasatiempos: me acompaña en el día a día y me inspira en lo personal y profesional.
        También disfruto de la lectura como forma de aprendizaje y desconexión.
      </li>
      <li class="item">
        Me apasiona todo lo relacionado con sistemas de salud, especialmente aquellos que permiten mejorar la gestión, la comunicación y la experiencia de pacientes y profesionales.
        Busco integrar tecnología con impacto humano.
      </li>
      <li class="item">
        Me desempeño en el quirófano dentro del área de salud, lo que me permite comprender en profundidad las necesidades reales del entorno hospitalario.
        Esta experiencia me motiva a combinar mis conocimientos técnicos con soluciones digitales que aporten valor al sistema sanitario.
      </li>
    </ul>
  </div>
</template>
<style scoped>
.intereses-contenedor {
  display: flex;
  position: relative;
  margin: 0 auto;
  max-width: 85%;
  padding: 2rem;
  background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
  border-radius: 12px;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.4);
  flex-direction: column;
  z-index: 1;
}

.contenedor-lista {
  list-style-type: none;
  padding: 1rem;
  margin-bottom: 5rem;
  color: #f0f6fc;
  font-size: 1.2rem;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.8);
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.item {
  position: relative;
  padding-left: 1.5rem;
  animation: fadeInUp 0.8s ease forwards;
  opacity: 0;
}

/* Puntito decorativo */
.item::before {
  content: '';
  position: absolute;
  left: 0;
  top: 0.6rem;
  width: 10px;
  height: 10px;
  background-color: #58a6ff;
  border-radius: 50%;
  box-shadow: 0 0 6px #58a6ff;
}

/* Animación moderna */
@keyframes fadeInUp {
  from {
    transform: translateY(20px);
    opacity: 0;
  }
  to {
    transform: translateY(0);
    opacity: 1;
  }
}

</style>

<template>
  <div class="uk-card uk-card-default uk-grid-collapse uk-child-width-1-2@s uk-margin uk-card-hover" uk-grid>
      <div class="uk-flex-last@s uk-card-media-right uk-cover-container">
          <img :src="actividad.RutaImg" alt="" uk-cover>
          <canvas width="600" height="400"></canvas>
      </div>
      <div>
          <div class="uk-card-body uk-text-left">
            <div class="uk-card-badge-left uk-label" :style="{ background: actividad.color_area + '!important' }">
              {{ actividad.area }}
            </div>
            <h3 class="uk-card-title"> {{ actividad.actividad }}</h3>
            <p class="uk-text-small uk-text-muted">
              Publicado: {{actividad.fechaLAnzamiento}} <br> Fecha inicio: {{actividad.fecha_inicio_formato}} <br> Duración: {{actividad.duracion}}.
            </p>
          </div>
      </div>
  </div>
</template>

<script>
export default {
  name: 'ActividadCardRight',
  props: {
    actividad: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
.uk-card-badge-left {
    position: absolute;
    top: 30px;
    left: 30px; 
    z-index: 1;
}
</style>
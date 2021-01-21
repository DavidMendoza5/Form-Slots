<template>
  <div class="container">
    <div class="badge bg-secondary">
      <button class="btn btn-primary" @click="componenteSeleccionado= 'IniciarSesion'">Iniciar sesión</button>
      <button class="btn btn-primary" @click="componenteSeleccionado= 'CambiarClave'">Cambiar contraseña</button>
      <hr>
      <!-- La etiqueta keep-alive evita que el componente se destruya, es una etiqueta exclusiva de Vue -->
      <keep-alive>
        <component :is="componenteSeleccionado"></component>
      </keep-alive>
    </div>
  </div>
</template>

<script>
import MostrarFormulario from './components/mostrarFormulario.vue'
import IniciarSesion from './components/iniciarSesion.vue'
import CambiarClave from './components/cambiarClave.vue'

export default {
  components: {
    MostrarFormulario,
    IniciarSesion,
    CambiarClave
  },
  data() {
    return {
      componenteSeleccionado: 'IniciarSesion'
    }
  }
}
</script>

<style scoped>
  h3 {
    color: red;
  }
</style>

<template>
    <form class="row g-3">
        <!-- La etiqueta slot recibe HTML y lo inserta dentro de esta misma, de esa forma podemos mandar distintas etiquetas HTML a un componente -->
        <slot name="titulo"></slot>
        <slot name="elementos"></slot>
        <slot name="boton"></slot>
    </form>
</template>

<script>
export default {
    
}
</script>

<style scoped>
    h3 {
        color: antiquewhite;
    }
</style>
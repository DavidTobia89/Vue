<script setup>
const props =defineProps(['cotizacion'])
</script>

<template>
     <div class="contenedor-resultado" >
        <h2>Cotización </h2>
        <div class="resultado">
          <img :src="'https://cryptocompare.com/' + cotizacion.IMAGEURL" alt="imagen cripto">
          <div>
            <p>El precio es de: <span>{{ props.cotizacion.PRICE }}</span></p>
            <p>El precio más alto del día: <span>{{ props.cotizacion.HIGHDAY }}</span></p>
            <p>El precio más bajo del día: <span>{{ props.cotizacion.LOWDAY }}</span></p>
            <p>Variación últimas 24 horas: <span>{{ props.cotizacion.CHANGEPCT24HOUR }}%</span></p>
            <p>ültima Actualización: <span>{{ props.cotizacion.LASTUPDATE }}</span></p>
          </div>
        </div>
      </div>
</template>
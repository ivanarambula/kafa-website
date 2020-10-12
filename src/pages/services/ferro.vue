<template>
    <service-layout>
        <!-- SimpleHero -->
        <section class="intro">
            <simple-hero>
                <template #cover>
                    <g-image src="../../assets/images/services/hero-ferro.jpg"></g-image>
                </template>
                <h1 class="title">Ferroviario</h1>
            </simple-hero>
        </section>

        <!--TextBanner-->
        <section class="description">
            <text-banner>
                <p>Para envío de grandes volúmenes de cualquier tipo de mercancía a México y Estados Unidos.</p>
            </text-banner>
        </section>

        <!--Single Column / FeaturesGrid-->
        <section class="features">
            <single-column>
                <section class="features-grid">
                    <div class="feature">
                        <p class="feature__name">Destinos</p>
                        <p class="feature__description">Terminales en la Ciudad de México, Silao, Gudalajara, Culiacán, Cd. Obregón, Hermosillo, Mexicali, Monterrey y todo Estados Unidos.</p>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Ruta</p>
                        <p class="feature__description">Servicio Intermodal Interpacífico.</p>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Equipo Disponible</p>
                        <ul class="feature__description">
                            <li>20' y 40' DC.</li>
                            <li>40' HC.</li>
                            <li>53' HC.</li>
                        </ul>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Tipo de Carga</p>
                        <ul class="feature__description">
                            <li>Seca.</li>
                            <li>Peligrosa.</li>
                        </ul>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Carga Mínima</p>
                        <p class="feature__description">Desde 1 contenedor.</p>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Cálculo del Costo</p>
                        <p class="feature__description">Por ruta y tipo de carga.</p>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Tiempo de Entrega</p>
                        <p class="feature__description">Días.</p>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Horarios</p>
                        <ul class="feature__description">
                            <li>Horario flexible para la carga / descarga del contenedor.</li>
                            <li>Llegadas y salidas diarias.</li>
                        </ul>
                    </div>
                </section>
            </single-column>
        </section>
    </service-layout>
</template>

<script>
import ServiceLayout from '../../layouts/ServiceLayout';
export default {
  name: 'ferro',
  components: { ServiceLayout }, 
  metaInfo: {
    title: 'Flare Starter'
  }
}
</script>

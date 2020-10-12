<template>
    <service-layout>
        <!-- SimpleHero -->
        <section class="intro">
            <simple-hero>
                <template #cover>
                    <g-image src="../../assets/images/services/hero-aerial.jpg"></g-image>
                </template>
                <h1 class="title">Aéreo</h1>
            </simple-hero>
        </section>

        <!--TextBanner-->
        <section class="description">
            <text-banner>
                <p>El mejor tiempo de entrega en envíos de carga seca y refrigerada a México y el mundo.</p>
            </text-banner>
        </section>

        <!--Single Column / FeaturesGrid-->
        <section class="features">
            <single-column>
                <section class="features-grid">
                    <div class="feature">
                        <p class="feature__name">Destinos</p>
                        <ul class="feature__description">
                            <li>Nacionales</li>
                            <li>Entregas en los principales aeropuertos de México, América, Asia y Europa.</li>
                        </ul>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Tipo de Carga</p>
                        <ul class="feature__description">
                            <li>Seca.</li>
                            <li>Refrigerada.</li>
                            <li>Urgente.</li>
                            <li>Peligrosa.</li>
                        </ul>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Tiempo de Entrega</p>
                        <p class="feature__description">Horas / Días</p>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Alianzas</p>
                        <ul class="feature__description">
                            <li>Aeroméxico.</li>
                            <li>Interjet.</li>
                            <li>Volaris.</li>
                            <li>Vivaerobus.</li>
                            <li>Vuelos Internacionales vía Los Angeles.</li>
                        </ul>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Horarios</p>
                        <p class="feature__description">Salidas diarias.</p>
                    </div>
                </section>
            </single-column>
        </section>
    </service-layout>
</template>

<script>
import ServiceLayout from '../../layouts/ServiceLayout';
export default {
  name: 'aerial',
  components: { ServiceLayout }, 
  metaInfo: {
    title: 'Flare Starter'
  }
}
</script>
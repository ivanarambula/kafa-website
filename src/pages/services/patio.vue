<template>
    <service-layout>
        <!-- SimpleHero -->
        <section class="intro">
            <simple-hero>
                <template #cover>
                    <g-image src="../../assets/images/patio.jpg"></g-image>
                </template>
                <h1 class="title">Patio</h1>
            </simple-hero>
        </section>

        <!--TextBanner-->
        <section class="description">
        </section>

        <!--Single Column / FeaturesGrid-->
        <section class="features">
            <single-column>
                <section class="features-grid">
                    <div class="feature">
                        <p class="feature__name">Ubicación</p>
                        <ul class="feature__description">
                            <li>El Sauzal, Ensenada, B.C.</li>
                            <li>Hermosillo, Son.</li>
                            <li>Guadalajara, Jal.</li>
                        </ul>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Tipo de Carga</p>
                        <ul class="feature__description">
                            <li>Contenedores cargados de importación o exportación.</li>
                            <li>Contenedores Refrigerados</li>
                            <li>Contenedores con carga peligrosa.</li>
                        </ul>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Sistemas de seguridad</p>
                        <ul class="feature__description">
                            <li>Guardia y alarma.</li>
                            <li>Video-vigilancia.</li>
                            <li>Registro de entradas y salidas.</li>
                        </ul>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Servicios adicionales</p>
                        <ul class="feature__description">
                            <li>Conexiones para contenedores refrigerados.</li>
                            <li>Maniobras de consolidación y desconsolidación.</li>
                            <li>Carga y descarga de contenedores llenos y vacíos.</li>
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
  name: 'patio',
  components: { ServiceLayout }, 
  metaInfo: {
    title: 'Flare Starter'
  }
}
</script>
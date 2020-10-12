<template>  
    <service-layout>
        <!-- SimpleHero -->
        <section class="intro">
            <simple-hero>
                <template #cover>
                    <g-image src="../../assets/images/services/hero-maritime-fcl.jpg"></g-image>
                </template>
                <h1 class="title">Marítimo FCL</h1>
            </simple-hero>
        </section>

        <!--TextBanner-->
        <section class="description">
            <text-banner>
                <p>Este tipo de flete te garantiza mayor rentabilidad por volumen, seguridad y flexibilidad en la entrega de tu mercancía de importación y exportación. Envía tus productos al otro lado del mundo con la asesoría de nuestros expertos en logística y recibe tu mercancía de importación mediante el método más confiable, seguro y eficiente.</p>
            </text-banner>
        </section>

        <!--Single Column / FeaturesGrid-->
        <section class="features">
            <single-column>
                <section class="features-grid">
                    <div class="feature">
                        <p class="feature__name">Destinos</p>
                        <p class="feature__description">Principales puertos en México, Asia, Europa, América y todo el mundo.</p>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Equipo Disponible</p>
                            <ul class="feature__description">
                                <li>20' y 40' DC.</li>
                                <li>40' HC.</li>
                                <li>40' RF.</li>
                                <li>20' y 40' FR.</li>
                                <li>20' y 40' OT.</li>
                            </ul>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Tipo de Carga</p>
                        <ul class="feature__description">
                            <li>Seca.</li>
                            <li>Refrigerada.</li>
                            <li>Peligrosa.</li>
                        </ul>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Carga Mínima</p>
                        <p class="feature__description">Desde 1 contenedor.</p>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Cálculo del Costo</p>
                        <p class="feature__description">Por contenedor.</p>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Tiempo de Entrega</p>
                        <p class="feature__description">Semanas.</p>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Monitoreo</p>
                        <p class="feature__description">A través de nuestra plataforma.</p>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Alianzas</p>
                        <ul class="feature__description">
                            <li>Cosco</li>
                            <li>APL</li>
                            <li>ONE</li>
                            <li>CMA-CGM</li>
                            <li>Hapag Lloyd</li>
                            <li>MSC</li>
                        </ul>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Servicios Adicionales</p>
                        <ul class="feature__description">
                            <li>Servicio de resguardo en patio o almacén.</li>
                            <li>Etiquetado de mercancía para importación / exportación.</li>
                            <li>Conexiones para contenedor refrigerado.</li>
                            <li>“Cross Docking”.</li>
                        </ul>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Horarios</p>
                        <ul class="feature__description">
                            <li>Horario flexible para la carga/descarga del contenedor.</li>
                            <li>Arribos y zarpes calendarizados semanales.</li>
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
  name: 'maritime-fcl',
  components: { ServiceLayout }, 
  metaInfo: {
    title: 'Flare Starter'
  }
}
</script>
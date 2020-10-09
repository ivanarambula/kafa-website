<template>
    <service-layout>
        <!-- SimpleHero -->
        <section class="intro">
            <simple-hero>
                <template #cover>
                    <g-image src="../../assets/images/warehouse.jpg"></g-image>
                </template>
                <h1 class="title">Almacenes</h1>
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
                        <p class="feature__name">Almacenes</p>
                        <ul class="feature__description">
                            <li>Ensenada - 800 m².</li>
                            <li>Tijuana Otay - 2,000 m².</li>
                            <li>Otay, CA (EE.UU.) - 2,000 m².</li>
                        </ul>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Equipamiento</p>
                        <ul class="feature__description">
                            <li>Racks.</li>
                            <li>Unidades para distribución de la mercancía.</li>
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
                        <p class="feature__name">Servicios Adicionales</p>
                        <ul class="feature__description">
                            <li>Maniobras de consolidación y desconsolidación.</li>
                            <li>Etiquetado de mercancía.</li>
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
  name: 'warehouse',
  components: { ServiceLayout }, 
  metaInfo: {
    title: 'Flare Starter'
  }
}
</script>

<template>
    <service-layout>
        <!-- SimpleHero -->
        <section class="intro">
            <simple-hero>
                <template #cover>
                    <g-image src="../../assets/images/services/hero-terrestrial.jpg"></g-image>
                </template>
                <h1 class="title">Terrestre</h1>
            </simple-hero>
        </section>

        <!--TextBanner-->
        <section class="description">
            <text-banner>
                <p>Total flexibilidad en rutas, equipo y tiempo de carga y descarga.</p>
            </text-banner>
        </section>

        <!--Single Column / FeaturesGrid-->
        <section class="features">
            <single-column>
                <section class="features-grid">
                    <div class="feature">
                        <p class="feature__name">Destinos</p>
                        <ul class="feature__description">
                            <li>Todo México.</li>
                            <li>EE.UU. y Canadá.</li>
                        </ul>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Equipo Disponible</p>
                        <ul class="feature__description">
                            <li>Cajas de 40', 48' y 53'.</li>
                            <li>Plataformas de 40', 48' y 53'.</li>
                            <li>Torton.</li>
                            <li>Rabón.</li>
                            <li>3.5 ton.</li>
                            <li>1 ton.</li>
                        </ul>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Tipo de Carga</p>
                        <ul class="feature__description">
                            <li>Seca.</li>
                            <li>Refrigerada.</li>
                            <li>Con sobre-dimensiones.</li>
                            <li>Con sobre-peso.</li>
                            <li>Hazmat o peligroso.</li>
                        </ul>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Carga Mínima</p>
                        <p class="feature__description">Desde 1 pallet.</p>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Cálculo del Costo</p>
                        <p class="feature__description">Por ruta y tipo de carga.</p>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Tiempo de Entrega</p>
                        <p class="feature__description">Horas / Días.</p>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Monitoreo</p>
                        <p class="feature__description">Vía GPS.</p>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Seguridad</p>
                        <ul class="feature__description">
                            <li>Todos los movimientos son realizados por autopistas.</li>
                            <li>Unidades con seguro.</li>
                            <li>Seguro a la carga.</li>
                        </ul>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Servicios Adicionales</p>
                        <ul class="feature__description">
                            <li>Doble operador.</li>
                            <li>Servicio de resguardo en patio o almacén.</li>
                            <li>Etiquetado de mercancía para importación / exportación.</li>
                        </ul>
                    </div>
                    <div class="feature">
                        <p class="feature__name">Horarios</p>
                        <p class="feature__description">24/7.</p>
                    </div>
                </section>
            </single-column>
        </section>
    </service-layout>
</template>


<script>
import ServiceLayout from '../../layouts/ServiceLayout';
export default {
  name: 'terrestrial',
  components: { ServiceLayout }, 
  metaInfo: {
    title: 'Flare Starter'
  }
}
</script>
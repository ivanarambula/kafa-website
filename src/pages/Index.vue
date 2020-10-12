<template>
  <base-layout>
      <!-- SimpleHero -->
      <section class="intro">
        <simple-hero>
          <template #cover>
            <g-image src="../assets/images/hero-image.jpg"></g-image>
          </template>
          <h1 class="title">Tu enlace global<br>con operación local</h1>
          <p class="description">Ofrecemos la red de servicios más robusta y flexible.</p>
          <a href="#services" class="our-services">Nuestros servicios</a>
        </simple-hero>
      </section>

      <!-- TripletColumns / Stats -->
      <section class="stats">
          <triplet-columns>
            <template v-slot:left>
                <span class="first__number">10K</span>
                <span class="first__text">Envíos</span>
            </template>
            <template v-slot:middle>
                <span class="second__number">100K</span>
                <span class="second__text">Toneladas</span>
                <span class="second__text">enviadas</span>
            </template>
            <template v-slot:right>
                <span class="third__text">Todo tipo de carga</span>
                <div class="third__grid">
                  <span>Seca</span>
                  <span>Peligrosa</span>
                  <span>Refrigerada</span>
                  <span>Valiosa</span>
                </div>
            </template>
          </triplet-columns>
      </section>

      <!-- TripletColumns / Service Row 1 -->
      <section class="service-row-1" id="services">
          <triplet-columns>
            <template v-slot:left>
                <span class="service__name">Marítimo FCL</span>
                <p class="service__description">Mayor rentabilidad por volumen, seguridad y flexibilidad en la entrega de tu mercancía de importación y exportación.</p>
                <g-link to="/services/maritime-fcl" class="service__button">Leer Más</g-link>
            </template>
            <template v-slot:middle>
              <g-image src="../assets/images/home-grid-1.jpg"></g-image>
            </template>
            <template v-slot:right>
                <span class="service__name">Marítimo LCL</span>
                <p class="service__description">Ideal para emprendedores y empresas que requieren el servicio marítimo sin la necesidad de enviar un contenedor completo.</p>
                <g-link to="/services/maritime-lcl" class="service__button">Leer Más</g-link>
            </template>
          </triplet-columns>
      </section>

      <!-- TripletColumns / Service Row 2 -->
      <section class="service-row-2">
          <triplet-columns>
            <template v-slot:left>
              <g-image src="../assets/images/home-grid-2.jpg"></g-image>
            </template>
            <template v-slot:middle>
                <span class="service__name">Terrestre</span>
                <p class="service__description">Total flexibilidad en rutas, equipo y tiempo de carga y descarga.</p>
                <g-link to="/services/terrestrial" class="service__button">Leer Más</g-link>
            </template>
            <template v-slot:right>
              <g-image src="../assets/images/home-grid-3.jpg"></g-image>
            </template>
          </triplet-columns>
      </section>

      <!-- TripletColumns / Service Row 3 -->
      <section class="service-row-3">
          <triplet-columns>
            <template v-slot:left>
                <span class="service__name">Ferroviario</span>
                <p class="service__description">Para envío de grandes volúmenes de cualquier tipo de mercancía a México y Estados Unidos.</p>
                <g-link to="/services/ferro" class="service__button">Leer Más</g-link>
            </template>
            <template v-slot:middle>
              <g-image src="../assets/images/home-grid-4.jpg"></g-image>
            </template>
            <template v-slot:right>
                <span class="service__name">Aéreo</span>
                <p class="service__description">El mejor tiempo de entrega en envíos de carga seca y refrigerada a México y el mundo.</p>
                <g-link to="/services/aerial" class="service__button">Leer Más</g-link>
            </template>
          </triplet-columns>
      </section>
      
      <!--TextBanner / Contact Us-->
      <section class="contact-us">
        <text-banner>
          <span>Contamos soluciones para el manejo de tu carga</span>
          <h2>en reposo y en movimiento</h2>
          <g-link to="/Contact" class="contact-btn">Contáctanos</g-link>
        </text-banner>
      </section>

      <!-- TwinColumns / Warehousing -->
      <section class="warehousing">
        <twin-columns>
          <template v-slot:left>
            <span class="service__name">Almacenes</span>
            <p class="service__description">Mayor rentabilidad por volumen, seguridad y flexibilidad en la entrega de tu mercancía de importación y exportación. </p>
            <g-link to="/services/warehouse" class="service__button">Leer Más</g-link>
          </template>
          <template v-slot:right>
            <g-image src="../assets/images/warehouse.jpg"></g-image>
          </template>
        </twin-columns>
      </section>

      <!-- TwinColumns / Patio -->
      <section class="patio">
        <twin-columns>
          <template v-slot:left>
            <g-image src="../assets/images/patio.jpg"></g-image>
          </template>
          <template v-slot:right>
            <span class="service__name">Patio</span>
            <p class="service__description">Mayor rentabilidad por volumen, seguridad y flexibilidad en la entrega de tu mercancía de importación y exportación.</p>
            <g-link to="/services/patio" class="service__button">Leer Más</g-link>
          </template>
        </twin-columns>
      </section>
  </base-layout>
</template>


<script>
import BaseLayout from '../layouts/BaseLayout';
export default { 
  name: 'Index',
  components: { BaseLayout }, 
  metaInfo: {
    title: 'Flare Starter'
  }
}
</script>

<style lang="scss">
body {
  .intro {
    .simple-hero {
      &__container {
        place-content: center left;
      }
      &__content {
        padding-top: rem(124px);
        span {
          text-transform: uppercase;
          letter-spacing: 2.4px;
        }
        .title {
          color: white;
          font-size: 60px;
          font-weight: 900;
          text-transform: uppercase;
          text-shadow: 0px 2px 4px rgba(0, 0, 0, 0.51);
          @include respond-to('small and down') {
              font-size: rem(28px);
          }
          @include respond-to('medium') {
              font-size: rem(34px);
          }
        }
        .description {
          color: white;
        }
        .our-services {
          @include button($brand-yellow, black);
          width: rem(250px);
          text-transform: uppercase;
          text-align: center;
          text-decoration: none;
          font-weight: 900;
        }
        &>* {
          position: unset;
        }
        @include respond-to("small and down") {
            padding-top: 0;
            width: 100%;
        }
        @include respond-to("medium") {
          padding-top: 0;
          width: 100%;
        }
      }
    }
  }
  .stats {
    .triplets-columns {
      background-color: $brand-blue-6;
      &__section {
        padding: rem(28px) 0;
      }
      &__column {
        align-self: center;
        span {
          display: block;
          color: white;
          text-transform: uppercase;
          font-size: rem(25px);
          font-weight: 900;
          vertical-align: middle;
          &.first {
            &__number {
              font-size: rem(60px);
            }
            &__text {
              font-size: rem(28px);
            }
          }
          &.second {
            &__number {
              font-size: rem(68px);
              text-align: center;
            }
            &__text {
              text-align: center;
              font-size: rem(25px);
              &:last-child {
                font-size: rem(30px);
              }
            }
          }
          @include respond-to("small and down") {
            line-height: 1.2;
          }
          @include respond-to("medium") {
            line-height: 1.2;
          }
        }
        .third {
          &__grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            grid-template-rows: repeat(2, 1fr);
            grid-row-gap: rem(8px);
            grid-column-gap: rem(8px);
            padding: 0 rem(5px);
            span {
              font-size: rem(16px);
            }
          }
          &__text {
            margin-bottom: rem(16px);
            font-size: rem(23px);
            display: inline-block;
            width: auto;
            padding: 0 rem(16px);
          }
        }
      }
      @include respond-to("small and down") {
        grid-row-gap: rem(34px);
        padding: rem(28px) 0;
        &__section {
          text-align: center;
          padding: 0;
        }
        &__column {
          .third {
            &__grid {
              grid-template-columns: repeat(1, 1fr);
              grid-template-rows: repeat(1, 1fr);
              grid-row-gap: rem(8px);
            }
            &__text {
              margin-bottom: rem(8px);
            }
          }
        }
      }
      @include respond-to("medium") {
        grid-row-gap: rem(34px);
        align-self: center;
        padding: rem(28px) 0;
        text-align: center;
        &__section {
          padding: 0;
        }
        &__column {
          .third {
            &__grid {
              grid-template-columns: repeat(1, 1fr);
              grid-template-rows: repeat(1, 1fr);
              grid-row-gap: rem(8px);
            }
          }
        }
      }
    }
  }
  .service-row-1, .service-row-2, .service-row-3 {
    .triplets-columns {
      &__column {
        padding: rem(24px);
        &--start, &--middle, &--end {
          height: rem(400px);
          .service {
            &__name {
              font-size: rem(21px);
              color: white;
              text-transform: uppercase;
              font-weight: 900;
              border-bottom: 3px solid $brand-orange;
              padding-bottom: rem(16px);
              margin: 0 0 16px;
              display: inline-block;
            }
            &__description {
              color: white;
              @include respond-to("large and up") {
                width: 85%;
              }
            }
            &__button {
              @include button($brand-yellow, black);
              width: auto;
              padding: rem(12px);
              text-transform: uppercase;
              text-align: center;
              text-decoration: none;
              font-weight: 900;
            }
          }
        }
      }
    }
  }
  .service-row-1 {
    .triplets-columns {
      background-color: $brand-blue-5;
      &__column {
        &--start {
          background-color: $brand-blue-4;
        }
        &--middle {
          padding: 0;
          img {
            width: 100%;
            height: 100%;
            object-fit: cover;
          }
        }
        &--end {
          background-color: $brand-blue-7;
        }
        @include respond-to("small and down") {
          &--start, &--end {
            height: unset;
          }
        }
        @include respond-to("medium") {
          &--start, &--end {
            height: auto;
          }
        }
      }
    }
  }
  .service-row-2 {
    .triplets-columns {
      background-color: $brand-blue-7;
      &__column {
        &--start {
          padding: 0;
          img {
            width: 100%;
            height: 100%;
            object-fit: cover;
          }
        }
        &--middle {
          background-color: $brand-blue-3;
        }
        &--end {
          padding: 0;
          img {
            width: 100%;
            height: 100%;
            object-fit: cover;
          }
        }
        @include respond-to("small and down") {
          &--middle {
            height: auto;
          }
        }
        @include respond-to("medium") {
          &--middle {
            height: auto;
          }
        }
      }
    }
  }
  .service-row-3 {
    .triplets-columns {
      background-color: $brand-blue-5;
      &__column {
        &--start {
          background-color: $brand-blue-2;
        }
        &--middle {
          padding: 0;
          img {
            width: 100%;
            height: 100%;
            object-fit: cover;
          }
        }
        &--end {
          background-color: $brand-blue-3;
        }
        @include respond-to("small and down") {
          &--start, &--end {
            height: auto;
          }
        }
        @include respond-to("medium") {
          &--start, &--end {
            height: auto;
          }
        }
      }
    }
  }
  .contact-us {
    .text-banner {
      padding: rem(124px) 0;
      background-color: $brand-blue-6;
      span {
        display: block;
        font-size: rem(24px);
        line-height: 1;
        font-weight: 900;
        text-transform: uppercase;
        margin-bottom: rem(24px);
      }
      h2 {
        color: white;
        font-weight: 900;
        margin-bottom: rem(30px);
        text-transform: uppercase;
      }
      .contact-btn {
        @include button($brand-yellow, black);
        width: auto;
        margin: 0 auto;
        padding: rem(12px);
        text-transform: uppercase;
        text-align: center;
        text-decoration: none;
        font-weight: 900;
      }
    }
  }

  .warehousing, .patio {
    .twin-columns {
      height: rem(336px);
      @include respond-to("small and down") {
        height: unset;
      }
      @include respond-to("medium") {
        height: unset;
      }
      .twins {
        &-section {
          &--start, &--end {
            .twins {
              &-column {
                &--start, &--end {
                  .service {
                    &__name {
                      font-size: rem(21px);
                      color: white;
                      text-transform: uppercase;
                      font-weight: 900;
                      border-bottom: 3px solid $brand-orange;
                      margin: 0 0 16px;
                      padding-bottom: rem(16px);
                      display: inline-block;
                    }
                    &__description {
                      color: white;
                      @include respond-to("large and up") {
                        width: 85%;
                      }
                    }
                    &__button {
                      @include button($brand-yellow, black);
                      width: auto;
                      padding: rem(12px);
                      text-transform: uppercase;
                      text-align: center;
                      text-decoration: none;
                      font-weight: 900;
                    }
                  }
                  img {
                    /*
                    height: rem(336px);
                    @include respond-to("small and down") {
                      height: unset;
                    }
                    @include respond-to("medium") {
                      height: unset;
                    }
                    */
                  }
                }
              }
            }
            @include respond-to("small and down") {
              height: rem(336px);
            }
            @include respond-to("medium") {
              height: rem(336px);
            }
          }
        }
      }
    }
  }
  
  .warehousing {
    background-color: $brand-blue-4;
    .twin-columns {
      .twins {
        &-section {
          &--start {
            .twins {
              &-column {
                &--start {
                  width: rem(336px);
                  justify-self: center;
                  padding: rem(24px);
                  @include respond-to("small and down") {
                    justify-self: left;
                  }
                  @include respond-to("medium") {
                    justify-self: left;
                  }
                }
              }
            }
          }
          &--end {
            padding: 0;
            img {
              width: 100%;
              height: 100%;
              object-fit: cover;
            }
            .twins {
              &-column {
                width: 100%;
                &--end {
                  padding: 0;
                }
              }
            }
          }
        }
      }
    }
  }
  .patio {
    background-color: $brand-blue-6;
    .twin-columns {
      .twins {
        &-section {
          &--start {
            padding: 0;
            img {
              width: 100%;
              height: 100%;
              object-fit: cover;
            }
            .twins {
              &-column {
                width: 100%;
                &--start {
                  padding: 0;
                }
              }
            }
          }
          &--end {
            .twins {
              &-column {
                &--end {
                  width: rem(336px);
                  padding: rem(24px);
                }
              }
            }
          }
        }
      }
    }
  }
}
</style>
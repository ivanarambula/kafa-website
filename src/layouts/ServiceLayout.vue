<template>
  <simple-layout>
    <template #nav-toggle></template>
    <template #nav-toggle-close></template>
    <template #logo><g-link to="/"><g-image class="logo" src="../assets/images/kafa-logo.svg"></g-image></g-link></template>
    <template #navigation>
      <g-link to="/services/maritime-fcl">Marítimo FCL</g-link>
      <g-link to="/services/maritime-lcl">Marítimo LCL</g-link>
      <g-link to="/services/terrestrial">Terrestre</g-link>
      <g-link to="/services/aerial">Aéreo</g-link>
      <g-link to="/services/ferro">Ferroviario</g-link>
      <g-link to="/contact">Contacto</g-link>
    </template>
    <base-page class="service">
      <slot></slot>
    </base-page>
    <template #footer>
      <no-column class="container">
        <g-image src="~/assets/images/kafa-logo.svg" alt="logo"></g-image>
        <div class="link-block">
          <div class="link-item">
            <g-link to="/privacy">Aviso de Privacidad</g-link>
          </div>
          <div class="link-item">
            <g-link to="/terms">Términos y Condiciones</g-link>
          </div>
        </div>
        <span>Derechos Reservados ®2020</span>
      </no-column>
    </template>
  </simple-layout>
</template>

<script>
  export default {
    name: 'ServiceLayout',
  };
</script>

<style lang="scss">
  .logo {
    height: 30px;
    width: auto;
  }
  .header {
    &__content {
      @include respond-to('large and up') {
        grid-template-columns: rem($header-logo-space-width) 1fr rem(120px);
      }
    }
    .main-nav {
      &__close-button {
        background-image: url('../assets/images/navigation-close-icon.svg');
      }
      &__primary {
        a {
          color: white;
          text-transform: uppercase;
          text-decoration: none;
          font-weight: 900;
          &:hover {
              color: $header-nav-hover-color;
          }
          &:active {
              color: $header-nav-active-color;
          }
        }
      }
      &--open {
        z-index: 2;
        text-align: center;
      }
    }
    &__nav-toggle {
      height: 14px;
      background-image: url('../assets/images/navigation-icon.svg');
    }
  }
  .base-page {
    &.service {
        .intro {
            .simple-hero {
                &__container {
                    place-content: start left;
                    @include respond-to("small and down") {
                      place-content: center left;
                    }
                }
                &__content {
                    color: white;
                    padding-top: rem(145px);
                    .title {
                        color: white;
                        font-size: 60px;
                        font-weight: 900;
                        text-transform: uppercase;
                        text-shadow: 0px 2px 4px rgba(0, 0, 0, 0.51);
                        @include respond-to('small and down') {
                            font-size: rem(34px);
                        }
                        @include respond-to('medium') {
                            font-size: rem(34px);
                        }
                    }
                    &>* {
                        position: unset;
                    }
                     @include respond-to("small and down") {
                      padding-top: 0;
                      width: 100%;
                    }
                    @include respond-to("medium") {
                      width: 100%;
                    }
                }
            }
        }
        .description {
            background-color: $brand-blue-6;
            .text-banner {
                padding: rem(48px);
                .slim-column {
                    @include respond-to("large and up") {
                        width: rem(815px);
                    }
                    p {
                        color: white;
                        line-height: 1.5;
                        font-size: rem(21px);
                        margin: 0 0 16px;
                    }
                }
            }
        }
        .features {
            background-color: $brand-blue-5;
            padding-bottom: $gutter-xxlarge; 
            .single-column {
                .features-grid {
                    @include gridline(4, 0, top);
                    .feature {
                        color: white;
                        padding: rem(24px);
                        min-height: rem(292px);
                        &__name {
                            color: white;
                            text-transform: uppercase;
                            font-size: rem(21px);
                            font-weight: 900;
                            border-bottom: 3px solid $brand-orange;
                            padding-bottom: rem(16px);
                            margin: 0 0 16px;
                            display: inline-block;
                            line-height: 1em;
                        }
                        &__description {
                            color: white;
                            margin: 0;
                            li {
                                padding-bottom: $gutter-small;
                                margin: 0;
                                line-height: 1.5;
                                color: white;
                                &:before {
                                    content: "- ";
                                    position: absolute;
                                    margin-left: - $gutter-small;
                                }
                            }
                            @include respond-to('large and up') {
                                width: 85%;
                            }
                        }
                        &:first-child, &:nth-of-type(8), &:nth-of-type(9) {
                            background-color: $brand-blue-4;
                        }
                        &:nth-of-type(2), &:nth-of-type(4), &:nth-of-type(5), &:nth-of-type(7), &:nth-of-type(10), &:nth-of-type(12) {
                            background-color: $brand-blue-7;
                        }
                        &:nth-of-type(3), &:nth-of-type(6), &:nth-of-type(11) {
                            background-color: $brand-blue-3;
                        }
                    }
                    @include respond-to("medium") {
                        @include gridline(3, 0, top);
                        .feature {
                            &:first-child, &:nth-of-type(6), &:nth-of-type(7) {
                                background-color: $brand-blue-4;
                            }
                            &:nth-of-type(2), &:nth-of-type(4), &:nth-of-type(6), &:nth-of-type(8), &:nth-of-type(10), &:nth-of-type(12) {
                                background-color: $brand-blue-7;
                            }
                            &:nth-of-type(3), &:nth-of-type(5), &:nth-of-type(11) {
                                background-color: $brand-blue-3;
                            }
                        }
                    }
                    @include respond-to("small and down") {
                        @include gridline(1, 0, top);
                        .feature {
                            &:nth-child(even) {
                                background-color: $brand-blue-7;
                            }
                            &:nth-child(odd) {
                                background-color: $brand-blue-3;
                            }
                            &:first-child, &:last-child {
                                background-color: $brand-blue-4;
                            }
                        }
                    }
                }
            }
        }
    }
  }
  .footer {
    .container {
      display: grid;
      grid-template-columns: 0.5fr 1fr 0.5fr;
      grid-template-rows: 100%;
      text-align: left;
      align-self: center;
      .link-block {
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-gap: 0;
        align-self: center;
        a {
          display: block;
          color: white;
          text-decoration: none;
          margin-bottom: 0.5rem;
        }
        @include respond-to("small and down") {
          grid-template-columns: 100%;
          grid-template-rows: auto auto auto;
        }
      }
      span {
        margin-bottom: 0.5rem;
        align-self: center;
      }
       @include respond-to("small and down") {
      text-align: center;
      grid-template-columns: 100%;
      grid-template-rows: 50px 1fr 50px;
      grid-row-gap: $gutter;
      img {
        margin: 0 auto;
      }
    }
    }
  }
</style>
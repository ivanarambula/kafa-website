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
    <base-page>
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
    name: 'BaseLayout',
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
  .legal {
    background-color: $brand-blue-5;
    padding: $gutter-xxlarge 0;
    .slim-column {
        color: white;
        img {
            margin-bottom: $gutter-large;
        }
        .title {
            color: white;
            font-size: 48px;
            font-weight: 900;
            text-transform: uppercase;
            text-shadow: 0px 2px 4px rgba(0, 0, 0, 0.51);
            margin: 0 0 16px;
        }
        h2 {
            color: white;
            font-weight: 900;
            font-size: 21px;
        }
        p {
          color: white;
        }
        ul {
            margin-bottom: $gutter;
            li {
              color: white;
              line-height: 1.5em;
              margin: 0;
            }
        }
    }
}
</style>
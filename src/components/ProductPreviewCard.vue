<script setup>

</script>

<template>
  <div class="product-preview-card">
    <div class="product-image-wrapper">
      <img src="@/assets/images/product-mobile.jpg" alt="" class="product-image-mobile">
      <img src="@/assets/images/product-desktop.jpg" alt="" class="product-image-desktop">
    </div>
    
    <section class="content-section">
      <p class="product-category">Perfume</p>
      <h1 class="heading">Gabrielle Essence Eau De Parfum</h1>
      <p class="product-description">
        A floral, solar and voluptuous interpretation composed by Olivier Polge,
        Perfumer-Creator for the House of CHANEL.
      </p>
      <div class="prices">
        <span class="sale-price">$149.99</span>
        <span class="original-price">$169.99</span>
      </div>
      <button class="add-to-cart-button">
        <svg width="15" height="16" xmlns="http://www.w3.org/2000/svg"><path d="M14.383 10.388a2.397 2.397 0 0 0-1.518-2.222l1.494-5.593a.8.8 0 0 0-.144-.695.8.8 0 0 0-.631-.28H2.637L2.373.591A.8.8 0 0 0 1.598 0H0v1.598h.983l1.982 7.4a.8.8 0 0 0 .799.59h8.222a.8.8 0 0 1 0 1.599H1.598a.8.8 0 1 0 0 1.598h.943a2.397 2.397 0 1 0 4.507 0h1.885a2.397 2.397 0 1 0 4.331-.376 2.397 2.397 0 0 0 1.12-2.021ZM11.26 7.99H4.395L3.068 3.196h9.477L11.26 7.991Zm-6.465 6.392a.8.8 0 1 1 0-1.598.8.8 0 0 1 0 1.598Zm6.393 0a.8.8 0 1 1 0-1.598.8.8 0 0 1 0 1.598Z" fill="#FFF"/></svg>
        <span>Add to Cart</span>
      </button>
    </section>
  </div>
</template>

<style scoped lang="scss">
@import '@/styles/base/typography';
@import '@/styles/base/media-queries';

.product-preview-card {
  --border-radius: 10px;
  
  max-width: calc(343 / 16 * 1rem);
  margin-inline: auto;
  background-color: var(--color-pure-white);
  border-radius: var(--border-radius);
  
  @media #{$laptop-and-bigger} {
    max-width: 37.5rem;
    display: grid;
    grid-template-columns: 1fr 1fr;
  }
  
  .product-image-mobile {
    border-radius: var(--border-radius) var(--border-radius) 0 0;
  }
  
  .product-image-desktop {
    display: none;
  }
  
  @media #{$laptop-and-bigger} {
    .product-image-mobile {
      display: none;
    }
    
    .product-image-desktop {
      border-radius: var(--border-radius) 0 0 var(--border-radius);
      display: block;
    }
  }
  
  .content-section {
    padding: 1.5rem;
    display: flex;
    flex-direction: column;
    
    @media #{$laptop-and-bigger} {
      padding: 2rem;
    }
    
    .product-category {
      @extend %typography-overline;
      text-transform: uppercase;
    }
    
    .heading {
      margin-block-start: 0.75rem;
      color: var(--color-gunmetal);
      @extend %typography-display;
      font-weight: 800;
      
      @media #{$laptop-and-bigger} {
        margin-block-start: 1.25rem;
      }
    }
    
    .product-description {
      margin-block-start: 1rem;
      @extend %typography-body;
      
      @media #{$laptop-and-bigger} {
        margin-block-start: 1.5rem;
      }
    }
    
    .prices {
      margin-block-start: 1.5rem;
      display: flex;
      align-items: center;
      gap: calc(19 / 16 * 1rem);
      
      @media #{$laptop-and-bigger} {
        margin-block-start: auto;
      }
      
      .sale-price {
        color: var(--color-deep-aquamarine);
        @extend %typography-display;
      }
      
      .original-price {
        font-family: 'Montserrat', sans-serif;
        font-size: calc(13 / 16 * 1rem);
        font-weight: 500;
        line-height: calc(23 / 13);
        text-decoration: line-through;
      }
    }
    
    .add-to-cart-button {
      margin-block-start: 1.25rem;
      padding-block: 1rem;
      color: var(--color-pure-white);
      background-color: var(--color-deep-aquamarine);
      border: none;
      border-radius: 8px;
      @extend %typography-button-text;
      cursor: pointer;
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 0.75rem;
      
      &:hover, &:focus-visible {
        background-color: var(--color-deep-aquamarine-hover);
      }
      
      @media #{$laptop-and-bigger} {
        margin-block-start: 1.875rem;
      }
    }
  }
}
</style>

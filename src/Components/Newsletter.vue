<template>
  <section class="newsletter-area">
    <div class="container">
      <div class="row justify-content-between">

        <!-- Newsletter Text -->
        <div class="col-12 col-lg-6">
          <div class="newsletter-text">
            <h2>Join our Newsletter</h2>
            <p></p>
          </div>
        </div>

        <!-- Newsletter Form -->
        <div class="col-12 col-lg-4">
          <div class="newsletter-form">
            <form>
              <input class="nl-email" placeholder="Your E-mail">
              <button class="input-button" @click.prevent="haSubmit">Submit</button>
            </form>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Newsletter',
  methods: {
    haSubmit() {
      return alert('Thank you for subscribing')
    }
  }
}
</script>

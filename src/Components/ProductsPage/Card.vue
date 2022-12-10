<template>
  <div>
    <transition-group name="fade" class="row" tag="div">
      <div v-for="item in CardArray" class="col-6 col-xl-4 col-lg-4 col-md-4 col-sm-6 col-xs-4 pb-3" :key="item.id">
          <div class="card">
            <img class="card-img-top" :src="item.img" alt="Card image cap">
            <div class="overlay">
              <button type="button" class="btn btn-outline-secondary btn-lg" @click="addtoCart(item)">Add +</button>
              <router-link to="/Info"><button type="button" class="btn btn-outline-secondary btn-lg" @click="sendInfo(item)">Info</button></router-link>
            </div>
            <div class="card-body">
              <h5 class="card-title">{{ item.title }}</h5>
              <p class="card-text">${{ item.price }}</p>
            </div>
          </div>
      </div>
    </transition-group>
  </div>

</template>

<script>
export default {
  props: ['CardArray'],
  name: 'Card',
  methods: {
    addtoCart(it) {
     this.$store.commit('inCart', it)
    },
    sendInfo(it) {
     this.$store.commit('addtoInfo', it)
    }
  }
}
</script>


<script >

export default {
    data(){
    return{
      sideMenuValue: 0,
      infomenu: 0,
        
    }
  },
  methods: {
    openside() {
            if (this.sideMenuValue) {
                this.sideMenuValue = 0
            } else {
                this.sideMenuValue = 1

            }
            console.log(this.sideMenuValue)
        
        },
        infoside() {
            if (this.infomenu) {
                this.infomenu = 0
            } else {
                this.infomenu = 1
            }
        },
    
    },

  
  }
  
</script>


<template>
  <div class="nav">
         <router-link :to="{ name: 'home' }" class="link" >home</router-link>
         <router-link :to="{ name: 'prenotaServizio' }" class="link"  >prenota tavolo</router-link>
         <router-link :to="{ name: 'prenota' }" class="link"  >prenota asporto</router-link>
         <router-link :to="{ name: 'chi-siamo' }" class="link"  >chi siamo</router-link>
         <router-link :to="{ name: 'Contatti' }" class="link"  >contatti</router-link>
         <router-link :to="{ name: 'menu' }" class="link"  >menu</router-link>
      </div>
</template>

<style lang="scss" scoped>
@use '../assets/styles/general.scss' as *;

.nav{
  background-color: $c-nav;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  padding: 3rem;

  .link{
    color: white;
    text-transform: uppercase;
    font-size: 22px;
  }
}
</style>

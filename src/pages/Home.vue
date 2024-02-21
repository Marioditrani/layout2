
<script >
  
  export default {
    data(){
    return{
        obs:1,
            carouselMain:[
                {
                    
                },
                {
                    img : "../assets/img/bigimage.png",
                    paragrafo : "Lorem ipsum dolor sit amet consectetur adipisicing elit. Error alias, molestiae iusto at magnam cumque exercitationem est culpa quae tempore maxime sed accusantium officia minima consectetur. Distinctio quaerat dolorem soluta!",
                    link : "PRENOTA TAVOLO",
                    titolo : "Titolo paragrafo1",
                },
                {
                    img : "",
                    paragrafo : "ipsum dolor sit amet consectetur adipisicing elit. Error alias, molestiae iusto at magnam cumque exercitationem est culpa quae tempore maxime sed accusantium officia minima consectetur. Distinctio quaerat dolorem soluta!",
                    link : "MENU",
                    titolo : "Titolo paragrafo2",
                },
                {
                    img : "",
                    paragrafo : "Lorem ipsum dolor sit amet consectetur adipisicing elit. Error alias, molestiae iusto at magnam cumque exercitationem est culpa quae tempore maxime sed accusantium officia minima consectetur. Distinctio quaerat dolorem soluta!",
                    link : "PRENOTA D'ASPORTO",
                    titolo : "Titolo paragrafo3",
                }
            ]
    }
  },
  methods: {
    imgright(){
        if(this.obs == 3){
            this.obs = 1
        }else{
            this.obs ++
        } 
       
    },
    imgleft(){
        if(this.obs == 1){
            this.obs = 3
            
        }else{
            this.obs --
            
        }
            
     }
    },

  
  }
</script>


<template>

<main>

    <div class="main" :class="this.obs == 1 ? 'img1': '',this.obs == 2 ? 'img2' : '',this.obs == 3 ? 'img3' : ''">
        <div class="left">
            <p>{{ this.carouselMain[obs].paragrafo }}</p>
        </div>
        <div class="right">
            <div class="top-right">
                <div class="paragrafo">
                    <h2>{{ carouselMain[obs].titolo }}</h2>
                    <p>{{ carouselMain[obs].paragrafo }}</p>
                    <span class="button">{{ carouselMain[obs].link }}</span>
                </div>
                <div class="button-carousel">
                    <div class="left-arrow">
                        <svg xmlns="http://www.w3.org/2000/svg" width="25" height="25" fill="currentColor" class="bi bi-arrow-up-square" viewBox="0 0 16 16" @click="imgleft">
                            <path fill-rule="evenodd" d="M15 2a1 1 0 0 0-1-1H2a1 1 0 0 0-1 1v12a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1zM0 2a2 2 0 0 1 2-2h12a2 2 0 0 1 2 2v12a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2zm8.5 9.5a.5.5 0 0 1-1 0V5.707L5.354 7.854a.5.5 0 1 1-.708-.708l3-3a.5.5 0 0 1 .708 0l3 3a.5.5 0 0 1-.708.708L8.5 5.707z"/>
                        </svg>
                    </div>
                    <div class="number">
                        <div class="active-image"><span>{{ this.obs }} / 3</span></div>
                    </div>
                    <div class="right-arrow">
                        <svg xmlns="http://www.w3.org/2000/svg" width="25" height="25" fill="currentColor" class="bi bi-arrow-down-square" viewBox="0 0 16 16" @click="imgright">
                            <path fill-rule="evenodd" d="M15 2a1 1 0 0 0-1-1H2a1 1 0 0 0-1 1v12a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1zM0 2a2 2 0 0 1 2-2h12a2 2 0 0 1 2 2v12a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2zm8.5 2.5a.5.5 0 0 0-1 0v5.793L5.354 8.146a.5.5 0 1 0-.708.708l3 3a.5.5 0 0 0 .708 0l3-3a.5.5 0 0 0-.708-.708L8.5 10.293z"/>
                        </svg>
                    </div>
                </div>
            </div>
            <div class="bottom-right">
            <div class="left-bottom">
                <h3>orari d'apertura</h3>
                <div class="container-og">
                    <div class="container-giorni">
                        <span>lunedi</span>
                        <span>martedi</span>
                        <span>mercoledi</span>
                        <span>giovedi</span>
                        <span>venerdi</span>
                        <span>sabato</span>
                        <span>domenica</span>
                    </div>
                    <div class="container-orari">
                        <span>chiuso</span>
                        <span>16-22</span>
                        <span>16-22</span>
                        <span>16-22</span>
                        <span>16-22</span>
                        <span>16-22</span>
                        <span>16-22</span>
                    </div>
                </div>
            </div>
            <div class="right-bottom">
                <h3>dove trovarci</h3>
                <h4>Via lorem ipsum 12, 34900 Citta</h4>
                <img src="../assets/img/maps.png" alt="">
            </div>
        </div>
        </div>
       
       
    </div>
    

    
</main>
  
</template>

<style lang="scss" scoped>
@use '../assets/styles/general.scss' as *;



.img1{
    background: url('../assets/img/bigimage.png');
    transition: all .5s linear;
}
.img2{
    background: url('https://ilfattoalimentare.it/wp-content/uploads/2022/12/Depositphotos_505971914_L-1.jpg');
    transition: all .5s linear;
}
.img3{
    background: url(../assets/img/bigimage.png);
    transition: all .5s linear;
}
main{
    width: 100%;
    height: 100%;
    overflow: hidden;
    
    .main{
        display: flex;
        width: 100%;
        height: 100%;
        background-repeat: no-repeat;
        background-size: cover;
        .left{
            width: 50%;
            height: 100%;
            display: flex;
            align-items: flex-end;
            padding: 3rem;
            p{
                background-color: $c-paragrafo;
                border-radius: 20px;
                padding: 1rem;
            }
        }
        .right{
            width: 60%;
            height: 100%;

            .top-right{
                height: 50%;
                display: flex;
                flex-direction: row-reverse;
                .button-carousel{
                    width: 20%;
                    height: 100%;
                    background-color: rgba(0, 0, 0, 0.719);
                    display: flex;
                    flex-direction: column;
                    justify-content: space-between;
                    align-items: center;
                    color: white;
                    padding: 4rem 2rem;
                }
                .paragrafo{
                    background-color:$c-paragrafo;
                    display: flex;
                    flex-direction: column;
                    justify-content: space-between;
                    align-items: center;
                    text-align: center;
                    padding: 2rem;
                        h2{
                            color: black;
                            font-size: 27px;
                            text-transform: uppercase;
                        }
                        p{
                            color: black;
                            font-size: 25px;
                            padding-top: 2rem;
                        }
                        .button{
                            background-color: white;
                            padding: 1rem 2rem;
                            margin-top: 2rem;
                        }
                }
            }
            .bottom-right{
            background-color: #3B3737;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 3rem;
            height: 50%;
            color: white;
            .left-bottom{
                width: 50%;
                h3{
                    padding: .5rem;
                    font-size: 22px;
                    text-transform: uppercase;
                }
                
                .container-og{
                    display: flex;
                    justify-content: space-between;
                    padding: 1rem;
                    .container-giorni, .container-orari{
                        display: flex;
                        flex-direction: column;
                        font-size: 20px;
                    }
                }
                
            }
            .right-bottom{
                display: flex;
                flex-direction: column;
                align-items: center;
                gap: 1rem;
                h3{
                    text-align: center;
                    padding: .5rem;
                    font-size: 22px;
                    text-transform: uppercase;
                }
                h4{
                    text-align: center;
                }
                img{
                    width: 200px;
                    border-radius: 20px;
                    border: 2px solid white;
                }
            }
        }
            
        }
    }

    
}

@media (max-width: 1600px) {
    .main{
        flex-direction: column;
        .left, .right{
            width: 100%!important;
        }
        .left{
            margin: 20rem 0 0;
            
        }
        .top-right{
            flex-direction: column-reverse!important;
            .button-carousel{
                width: 100%!important;
                padding: 1rem!important;
                flex-direction: row  !important;
                justify-content: center  !important;
                gap: 20px;
            }
        }
    }
}


</style>

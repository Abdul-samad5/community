<template>
    <div class="row">

        <div class="col-lg-5 left">
            <div class="centred" style="margin-top:70px;">
                <img src="img/logo.png" alt="" class="logo">
                <div class="name">
                    <p class="eko">EkoMarket </p>
                    <p class="pick">Pickup</p>
                </div>
            </div>

            <div class="centred">
                <Carousel
                    :itemsToShow="1"
                    :wrapAround="true"
                    :autoplay="5000"
                    :transition="300"
                    :itemsToScroll="1"
                >
                    <slide :index="1">

                        <div>
                            <img src="img/slide1.png" alt="" class="slideImage">

                            <div class="slide-words text-left">
                                <p class="title">
                                    <span>Shop with us</span> and get your good deliver at your door steps
                                </p>

                                <p class="desc">
                                    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam sed id pulvinar ultrices leo urna accumsan imperdiet
                                    mattis. Viverra vestibulum bibendum amet, sed. Gravida ipsum diam mollis morbi vestibulum ornare dolor pharetra
                                    nascetur. Vulputate neque tempus vitae tellus malesuada.
                                </p>
                            </div>

                        </div>


                    </slide>
                    <slide :index="2">
                        <div>
                            <img src="img/slide2.png" alt="" class="slideImage mt-3">

                            <div class="slide-words text-left">
                                <p class="title">
                                    <span>Shop with us</span> and get your good deliver at your door steps
                                </p>

                                <p class="desc">
                                    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam sed id pulvinar ultrices leo urna accumsan imperdiet
                                    mattis. Viverra vestibulum bibendum amet, sed. Gravida ipsum diam mollis morbi vestibulum ornare dolor pharetra
                                    nascetur. Vulputate neque tempus vitae tellus malesuada.
                                </p>
                            </div>

                        </div>
                    </slide>
                    <slide :index="3">
                        <div>
                            <img src="img/slide3.png" alt="" class="slideImage">

                            <div class="slide-words text-left">
                                <p class="title">
                                    <span>Shop with us</span> and get your good deliver at your door steps
                                </p>

                                <p class="desc">
                                    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam sed id pulvinar ultrices leo urna accumsan imperdiet
                                    mattis. Viverra vestibulum bibendum amet, sed. Gravida ipsum diam mollis morbi vestibulum ornare dolor pharetra
                                    nascetur. Vulputate neque tempus vitae tellus malesuada.
                                </p>
                            </div>

                        </div>
                    </slide>

                    <template #addons>
                        <pagination />
                    </template>

                </Carousel>
            </div>

        </div>

        <div class="col-lg-7">
            <div class="right_container centredH">
                <div>


                    <p class="title">
                        <span>Hi, Welcome aboard !, </span> Tell us who you are
                    </p>

                    <p class="desc">
                        As a <span>Buyer </span> we can match products, goods that meets your need on the platform ipsum diam mollis morbi
                        vestibulum ornare dolor pharetra nascetur. Vulputate neque tempus vitae tellus malesuada. <br><br>
                        As a <span>Vendor</span> we can  ipsum diam mollis morbi vestibulum ornare dolor pharetra nascetur. Vulputate
                        neque tempus vitae tellus malesuada

                    </p>

                    <div class="row mt-4 ml-1">
                        <div class="col-md-6 box mr-3">
                            <div class="side">
                            </div>

                            <div class="centredH" style="height:100%;width:60%">
                                <img src="img/vendor.png" alt="">
                                <p class="sideWord">Vendor</p>
                            </div>



                        </div>

                        <div class="col-md-6 box">
                            <div class="side">
                            </div>

                            <div class="centredH" style="height:100%;width:60%">
                                <img src="img/buyer.png" alt="">
                                <p class="sideWord">Buyer</p>
                            </div>
                        </div>
                    </div>

                    <Link :href="route('login')" class="" id=""><button class="continue">Continue</button></Link>
                </div>
            </div>
        </div>

    </div>
</template>

<script>
import { Head, Link } from "@inertiajs/inertia-vue3";
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide, Pagination, Navigation } from "vue3-carousel";
export default {

    name: "Dashboard",
    data() {
        return {



        };
    },
    props: {
        canLogin: Boolean,
        canRegister: Boolean,
        laravelVersion: String,
        phpVersion: String,
    },
    components: {
        Carousel,
        Slide,
        Pagination,
        Navigation,
        Link
    },
    computed: {},
    methods: {

    },
    mounted() {



    },

    beforeMount() {
    },
}
</script>

<style scoped>
    .left{
        background: #FFEDED;
        height:100vh;
    }
    .centred{
        display: flex;
        justify-content: center;
    }

    .centredH{
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .logo{
        width: 65.31px;
        height: 60.81px;
    }

    .name{
        font-family: 'Nunito';
        font-style: normal;
        font-weight: 700;
        font-size: 32.5424px;
        line-height: 44px;

        color: #263238;
    }

    .pick{
        font-size: 21.6949px;
        margin-top: -20px;
    }

    .slideImage{
        width: 400px;
        height: 266.67px;
        margin: auto;
    }
    .slide-words{
        width:90%;
        margin:auto;
    }



    .title{
        font-family: 'Poppins';
        font-style: normal;
        font-weight: 600;
        font-size: 34px;
        line-height: 51px;

        color: #000000;
    }

    .title > span, .desc > span{
        color: #FF725E;
    }

    .desc{
        font-family: 'Poppins';
        font-style: normal;
        font-weight: 400;
        font-size: 16px;
        line-height: 24px;
        color: #263238;
    }

    .carousel__pagination{
        justify-content: left !important;
        margin-left:5%;
    }
    .carousel__pagination-button{
        background-color: rgba(38, 50, 56, 0.5) !important;
    }


    .carousel__pagination-button--active{
        background-color: #000000 !important;
    }

    .right_container{
        height:100vh;
        width:70%;
        margin:auto;
    }



    .box{
        width: 47%;
        height: 146.39px;
        background: #FFFFFF;
        border: 1.5px solid #FF725E;
        position:relative;
    }

    .side{
        position: absolute;
        right: -11%;
        top: -5%;
        border-left: 5px solid transparent;
        border-right: 5px solid transparent;
        border-bottom: 0;
        border-width: 50px;
        transform: rotate(225deg);
    }

    .sideWord{
        font-family: 'Poppins';
        font-style: normal;
        font-weight: 500;
        font-size: 28px;
        line-height: 42px;
        color: #707070;
    }

    @media screen and (max-width:850px) {
        .right_container{
            margin-top:-130px;
            padding-bottom:50px;
        }

        .left{
            height:670px;
        }

        .sideWord{
            font-size:15px;
        }
    }

    @media screen and (max-width:500px) {
        .right_container{
            margin-top:80px;
            padding-bottom:50px;
        }

        .left{
            min-height:870px;
        }

        .sideWord{
            font-size:15px;
        }

        .side{
            right:-21%;
        }
    }



    .continue{
        width: 329px;
        height: 60px;
        color:white;
        background: #FF725E;
        margin-top: 50px;
        font-family: 'Poppins';
        font-style: normal;
        font-weight: 400;
        font-size: 20px;
        line-height: 30px;
    }

    @media screen and (max-width:350px) {
        .right_container{
            margin-top:150px;
            padding-bottom:50px;
            padding-left:2px;
        }

        .left{
            min-height:870px;
        }

        .sideWord, .desc{
            font-size:12px;
        }

        .side{
            right:-21%;
        }

        .title{
            font-size:28px;
        }

        .continue{
            width:300px;
        }
    }




</style>

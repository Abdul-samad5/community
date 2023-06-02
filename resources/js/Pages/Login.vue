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

                    <div class="d-flex">
                        <img src="img/login.png" alt="">
                        <p class="title ml-2">
                            Login
                        </p>
                    </div>


                    <p class="desc mt-2">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lorem vulputate ac, volutpat cursus.
                    </p>

                    <div class="row">
                        <input type="text" placeholder="Email">
                        <input type="text" placeholder="Password">
                    </div>

                    <p class="desc mt-5 ml-1">
                        Forgot Password?
                    </p>
                    <Link :href="route('dashboard')" >
                        <button class="continue">Login</button>
                    </Link>


                    <Link :href="route('register')" >
                        <p class="desc mt-4 ml-1">
                            <span>Don’t have an account? Register now</span>
                        </p>
                    </Link>
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
        font-weight: 500;
        font-size: 26.5974px;
        line-height: 40px;
        /* identical to box height */


        color: #FF725E;
    }

    input{
        width:95%;
        margin:auto;
        margin-top:30px;
        border-color:black;

    }

    .desc{
        font-family: 'Poppins';
        font-style: normal;
        font-weight: 400;
        font-size: 16px;
        line-height: 24px;
        color: #263238;
    }

    .title > span, .desc > span{
        color: #FF725E;
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
        width:50%;
        margin:auto;
    }



    @media screen and (max-width:850px) {
        .right_container{
            margin-top:-130px;
            width:80%;
            margin:auto;
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
        width:100%;
        margin:auto;
        height: 50px;
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

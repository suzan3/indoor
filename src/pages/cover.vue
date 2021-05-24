<template>
<q-page class="flex flex-c-center flex-flex-end cover">
    <div class="social-media">
        <div class="q-mx-Cmd">Instagram</div>
        <div class="q-mx-Cmd">facebook</div>
        <div class="q-mx-Cmd">twitter</div>
    </div>
    <div class="download-app">
        <div class="q-mb-sm getApp">Get <span class="bold-font"> Mobile Application </span>now!</div>
        <div class="row">
            <div class="col-6">
                <q-btn color="white">
                    <div class="row items-center no-wrap">
                        <!-- <q-icon left name="apple" /> -->
                        <img class="q-mr-sm" src="~assets/Apple_logo.png" alt="">
                        <div class="text-left btn">
                            <span class="download"> Download on the </span>
                            <br>
                            App Store
                        </div>
                    </div>
                </q-btn>
            </div>
            <div class="col-6">
                <q-btn color="white">
                    <div class="row items-center no-wrap">
                        <!-- <q-icon left name="apple" /> -->
                        <img class="q-mr-sm" src="~assets/play-store.png" alt="">
                        <div class="text-left btn">
                            <span class="download"> Get it on </span>
                            <br>
                            Google Play
                        </div>
                    </div>
                </q-btn>
            </div>
        </div>
    </div>
    <div class="flex flex-center text-center">
        <div class="row">
            <div class="col-12 text">
                disrupt-<img src="~assets/x.png" width="75px">
            </div>
            <div class="col-12 title">
                indoor air monitoring
            </div>
            <div class="col-sm-6 col-10 q-mx-auto text-center description">
                Introducing Ignite Shield IoT Platform Solution for Indoor Air Quality Monitoring (IAQ) where Air Quality Sensors, will play an important role in providing various sensor tracking.
            </div>
        </div>
    </div>
    <div class="down">
            <img @click="goto()" src="~assets/down-arrow.png">
    </div>
</q-page>
</template>

<style lang="scss">
.cover {
    .q-mx-Cmd{
    margin-left: 12px !important;
    margin-right: 13px !important;
    }
    .cBtn{
        padding: 0 !important;
        &:hover,&:focus{
            background-color: transparent !important;
        }
    }
    .getApp {
        font-family: 'Roboto-Regular';
        font-size: 20px;

        span {
            font-family: 'Roboto-Bold';
        }
    }

    .q-btn__wrapper:before {
        box-shadow: none !important;
    }

    background-image: url('~assets/Rectangle.png'),
    url('~assets/cover-bg.png');
    background-repeat: no-repeat,
    no-repeat;
    background-position: left,
    center;
    background-size: 50% 100%,
    cover;

    @media only screen and (max-width: 775px) {
        .text {
            font-size: 70px !important;

            img {
                width: 45px !important;
            }
        }

        .title {
            font-size: 25px !important;
        }

        .description {
            font-size: 15px !important;
        }

        .download-app {
            right: auto !important;
            bottom: 80px !important;
        }

        .down {
            height: 75px !important;
            width: 70px !important;
            margin-top: 35px !important;
        }

        .q-btn {
            width: 152px !important;
        }

        .download {
            font-size: 11px !important;
        }

        .btn {
            font-size: 14px !important;
        }

        .q-btn__wrapper {
            padding: 0 !important;
        }

        .q-btn__wrapper:before {
            box-shadow: none !important;
        }

        .social-media {
            right: -109px !important;
        }
    }

    .download-app {
        font-family: 'Roboto-Regular';
        color: white;
        font-size: 20px;
        position: absolute;
        bottom: 40px;
        right: 50px;
    }

    .q-btn {
        width: 200px;
        border-radius: 0 !important;
        padding: 10px;
    }

    .download {
        font-size: 12px;
        font-family: 'Roboto-Regular';

    }

    .bold-font {
        font-family: 'Roboto-Bold' !important;
    }

    .btn {
        color: black;
        font-size: 16px;
        line-height: 20px;
        font-family: 'Roboto-Bold';
    }

    .q-icon {
        color: black;
    }

    .down {
        width: 130px;
        height: 85px;
        background-color: #20313B;
        text-align: center;
        justify-content: center;
        display: flex;
        padding: 1.5rem;
        cursor: pointer;
    }

    .text {
        color: white;
        font-size: 120px;
        font-weight: bold;
    }

    .title {
        color: white;
        font-size: 32px;
        font-family: 'Roboto-Bold';
    }

    .description {
        color: white;
        font-size: 20px;
        font-family: 'segoe-ui';
    }

    .social-media {
        cursor: pointer;
        font-family: 'Roboto-Bold';
        font-size: 15px;
        color: white;
        position: absolute;
        right: -95px;
        top: 50%;
        display: flex;
        transform: rotate(270deg);
    }
}

@media only screen and (min-width: 776px) and (max-width: 1050px) {
    .download-app {
        bottom: 20px !important;
    }

    .flex-c-center {
        justify-content: left !important;
    }
}

.flex-c-center {
    justify-content: center;
}

.flex-flex-end {
    align-items: flex-end !important;
}
html{
      scroll-behavior: smooth;

}
</style>

<script>
export default {
    name: 'cover',
    methods: {
        goto() {
            window.scrollTo(0, 600);
        }
    }
}
</script>

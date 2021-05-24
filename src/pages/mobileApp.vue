<template>
<q-page class="flex flex-center app q-my-xl">
    <div class="row w-100">
        <div class="col-12 text-center center title">
            Mobile Application
        </div>
        <div class="line q-ml-auto"></div>
        <div class="col-7 q-mx-auto q-mt-lg text-center description">
            Ignite Shield's Indoor Air Quality Monitoring (IAQ)- loT Solution
        </div>
    </div>
    <div class="row content w-100 q-mt-xl">
        <div class="col-md-6 col-12 mobiles">

        </div>
        <div class="col-md-6 col-12 q-pl-lg">
            <div class="title">
                Mobile app provided services
            </div>
            <div v-for='index in ListServices' :key='index' class="description">
                {{index.value}}
            </div>
            <div class="row q-px-xl">
                <div class="col-md-6 col-12 q-mt-xl">
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
                <div class="col-md-6 col-12 q-mt-xl">
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
    </div>
</q-page>
</template>

<style lang="scss">
.app {
    @media only screen and (min-width: 501px) and (max-width: 1023px){
        .mobiles{
            background-size: contain !important;
            height: 400px !important;
        }

    }
     @media only screen and (max-width: 500px){
        .mobiles{
            background-size: cover !important;
            height: 370px !important;
        }
        .title{
            font-size: 22px !important;
        }
        .description{
            font-size: 16px !important;
        }

    }
    .q-btn {
        width: 200px;
        border-radius: 0 !important;
        padding: 5px;
    }

    .download {
        font-size: 12px;
    }

    .bold-font {
        font-family: 'Roboto-Bold' !important;
    }

    .btn {
        color: black;
        font-size: 16px;
        line-height: 20px;
    }

    .q-icon {
        color: black;
    }

    .w-100 {
        width: 100%;
    }

    .content {
        background-image: url('~assets/AppRectangle.png');
        background-position: center;
        background-repeat: no-repeat;
        background-size: contain;

        .title {
            font-family: "Roboto-Bold";
            font-size: 32px;
        }

        .description {
            font-family: "Roboto-Regular";
            font-size: 25px;

            &:before {
                content: "•";
                color: #1e8d77
            }
        }
    }

    .title {
        color: black;
        font-family: "Roboto-Bold";
        font-size: 62px;
    }

    .line {
        background-color: #1e8d77;
        height: 4px !important;
        width: 50%;
    }

    .description {
        font-family: 'Roboto-Regular';
        font-size: 20px;
        color: black;
    }

    .mobiles {
        background-image: url('~assets/mobiles.png');
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
        height: 565px;
    }
}
</style>

<script>
const services = [{
        value: 'Live Weather Monitoring Linked to Live Forecast'
    },
    {
        value: 'View Analytics and Recommendations'
    },
    {
        value: 'IAQ Parameter Index Awareness'
    },
    {
        value: 'Detailed IAQ Device Readings'
    },
    {
        value: 'Get Real-time IAQ Notifications'
    },
    {
        value: 'Alarm Levels Set up'
    },
    {
        value: 'Customized Alerts'
    },
    {
        value: 'User Friendly Mobile App'
    },
]
export default {
    name: "mobileApp",
    components: {},
    data() {
        return {
            ListServices: services,
        }
    }
};
</script>

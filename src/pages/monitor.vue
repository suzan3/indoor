<template>
<q-page class="flex flex-center monitor q-my-xl">
    <div class="row">
        <div class="col-12 text-center center title">
            What We Monitor
        </div>
        <div class="line"></div>
        <div class="col-7 q-mx-auto q-mt-lg text-center description">
            At Disrupt-X, introducing Ignite Shield's loT Platform Solution for
            Water Tank Monitoring where the Device will have an important role in
            providing accurate Water Tank sensor data for an accurate monitoring of
            Water Quality
        </div>
    </div>
    <div class="row w-100 q-mt-xl">
        <div class="col-md-6 col-12 left-section flex flex-center q-pa-lg">
            <q-list bordered>

                <q-item v-for='index in ListItems' :key='index' class="q-my-xl" clickable v-ripple>
                    <q-item-section avatar>
                        <q-avatar>
                            <img :src="index.icon">
                        </q-avatar>
                    </q-item-section>

                    <q-item-section>
                        <q-item-label class="text" lines="1">{{index.text}}</q-item-label>
                        <q-item-label caption lines="2">
                            <span class="sub-text q-mt-md">{{index.sub_text}}</span>
                        </q-item-label>
                    </q-item-section>

                </q-item>
            </q-list>
            <div class="center-image d-none">

            </div>
        </div>
        <div class="col-12 d-block image text-center">
                <img src="~assets/TVOC.png" width="40%" alt="">
        </div>
        <div class="col-md-5 q-ml-auto q-pr-xl col-12 right-section">
            <div class="title">
                Integrate Your Own
                Hardware
            </div>
            <div class="description">
                At Disrupt-X, we introduce Ignite Shield loT Platform Solution for Indoor Air Quality Monitoring (IAQ) where Air Quality Sensors, playing an important role, is providing various sensor tracking such as Temperature Monitoring, Humidity Monitoring, C02 Monitoring, and much more.
            </div>
            <div class="row q-mt-md">
                <div class="col-5">
                    <div v-for='(item) in ListFeatures.splice(0,ListFeatures.length/2 + 1)' :key="item" class="text">
                        {{item.value}}
                    </div>
                </div>
                <div class="col-2">
                    <q-separator class="q-mx-auto" vertical />
                </div>
                <div class="col-5">
                    <div v-for='(item) in ListFeatures.splice(0,ListFeatures.length)' :key="item" class="text">
                        {{item.value}}
                    </div>
                </div>
            </div>
        </div>
    </div>
</q-page>
</template>

<style lang="scss">
.monitor {
    @media only screen and (max-width: 1023px) {
     .right-section{
         padding-left: 10px;
         .text{
             font-size: 12px !important;
         }
     }
    }
    @media only screen  and (max-width: 550px) {
     .image{
         img{
             width: 75% !important;
         }
     }
    }
    @media only screen and(max-width: 1023px) {
     .d-none{
        display: none !important;
     }
     .d-block{
         display: block !important;
     }
    }
    .d-block{
        display: none ;
    }
    .center-image {
        background-image: url('~assets/TVOC.png');
        background-position: center;
        background-repeat: no-repeat;
        background-size: 100% 50%;
        width: 35%;
        left: 30%;
        height: 100%;
        position: absolute;
    }

    .q-avatar {
        border-radius: 0 !important;
        width: 53px !important;
        height: 59px !important;
    }

    .q-avatar__content .overflow-hidden {
        overflow: auto !important;
    }

    .q-avatar img:not(.q-icon) {
        height: auto !important;
        width: auto !important;
    }

    .q-list--bordered {
        border: none;
    }

    .w-100 {
        width: 100%;
    }

    .left-section {
        background-color: #20313B;

        .text {
            font-size: 32px;
            color: #FFFFFF;
            font-family: 'Roboto-Bold';
        }

        .sub-text {
            color: #FFFFFF;
            font-size: 20px;
            font-family: 'Roboto-Light';
        }
    }

    .right-section {
        .q-separator--vertical {
            width: 3px !important;
            height: 100% !important;
        }
        .q-separator{
            background-color: black;
        }
        .title {
            font-size: 60px;
            font-family: 'Roboto-Regular';
            line-height: 70px;
        }

        .description {
            font-size: 20px;
            font-family: 'Roboto-Regular';
        }

        .text {
            font-size: 25px;
            font-family: 'Roboto-Bold';
        }
    }

    .q-item__label {
        color: white;
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

}
</style>

<script>
const items = [{
        text: 'Connectivity',
        sub_text: 'Sigfox / 4G',
        icon: require('assets/first.png'),
    },
    {
        text: 'Sensor Life',
        sub_text: 'Up to 5 Years',
        icon: require('assets/second.png'),
    },
    {
        text: 'Battery Life',
        sub_text: 'Up to 5 Years',
        icon: require('assets/third.png'),
    }

];
const features = [{
        value: 'No Cables Required'
    },
    {
        value: 'Formaldehyde'
    },
    {
        value: 'PM 1/ PM 2.5/ PM 10'
    },
    {
        value: 'CH20'
    },
    {
        value: 'Dew Point'
    },
    {
        value: 'Barometer'
    },
    {
        value: 'Temperature'
    },
    {
        value: 'Humidity'
    },
    {
        value: 'CO2'
    },
    {
        value: 'TVOC'
    },
    {
        value: 'CO'
    },
]
export default {
    name: "monitor",
    components: {},
    data() {
        return {
            ListItems: items,
            ListFeatures: features
        }
    }
};
</script>

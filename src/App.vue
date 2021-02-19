<template>
<v-app>

  <v-main>
    <HelloWorld />

    <v-card class="mx-auto my-12 rounded-card" max-width="300">

      <v-card-text class="pa-0">
        <div class="priceTable">
          <div class="most-popular">Most popular</div>
          <div class="priceTableContainer">

            <div class="module">
              <div class="upperpart">

                <div class="paylable">You Pay</div>
                <div> <span class="price"> AED 125 </span> <span class="color-pink">/month</span></div>
                <div class="tax">
                  For 12 months + 5% VAT <span>/month</span>
                </div>
                <v-divider class="custom-card-divider"></v-divider>
                <div class="payget">You Get</div>
                <div class="planname">Power Plan 125</div>
                <v-divider class="custom-card-divider"></v-divider>
                <div class="plandetail">
                  <div class="planrow">
                    <p class=" cross">13</p> <b class="font28">26 GB</b>National Data
                  </div>
                  <div class="planrow"><b>100</b>Flexi minutes</div>
                </div>
                <v-divider class="custom-card-divider"></v-divider>
                <div class="planterms">
                  <div class="term">
                    <v-icon>
                      mdi-check
                    </v-icon>
                    No activation fee.Save AED 125
                  </div>
                  <div class="term">
                    <v-icon>
                      mdi-check
                    </v-icon>
                    4 GB free data on WiFi UAE
                  </div>
                </div>
              </div>
              <div class="footerpart">
                <div class="limitedOfferSection">
                  <div class="x-small limitedTimeOffer">
                    Limited time offer
                  </div>
                  <div class="limitedTimeOfferText">
                    <b>The Entertainer</b> on us for 12 months
                  </div>
                </div>

              </div>
              <v-card-actions class="footer ma-0">
                <div class="whatyouget">What you get</div>
                <div class="selectButton">
                  <v-btn class="btnSelect">Select</v-btn>
                </div>
              </v-card-actions>
            </div>
          </div>
        </div>
      </v-card-text>

    </v-card>

  </v-main>

</v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    HelloWorld,
  },
  computed: {
    createBackgroundString() {
      return `linear-gradient(to bottom, #cc1eac, #576abc, #28a9cc) 0 0 1 100%`;
    }
  },
  data() {
    return {
      items: [{
          src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
        },
      ],
    }
  },
};
</script>

<style scoped>
.v-chip.ongoing {
  background: #ffaa2c;
}

.custom-card-divider {
  margin-bottom: 10px;
  margin-top: 10px;
}

.rounded-card {
  border-radius: 15px !important;
}

.color-pink {
  color: #cc1eac;
}

@import url("https://fonts.googleapis.com/css2?family=Montserrat&display=swap");

.priceTable {
  background: #f7f7f7;
  border-radius: 10px;
}

.module {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding: 5px 15px 15px 15px;
  border-radius: 10px;
  background: #fff;
  color: white;
  border-width: 6px;
  border-style: solid;
  height: 500px;
  border-image: linear-gradient(to bottom, #cc1eac, #576abc, #28a9cc) 0 0 1 100%;
}

.paylable {
  color: #cc1eac;
  font-size: 12px;
}

.payget {
  color: #28a8cb;
}

.priceTableContainer {
  border-radius: 10px;
  overflow: hidden;
  height: 500px;
}

.price {
  color: #cc1eac;
  font-weight: bold;
  font-size: 1.2rem;
  margin-bottom: 5px;
}

.tax {
  color: #000;
  font-size: 0.8rem;
}

.planname {
  color: #28a8cb;
  font-weight: bold;
  font-size: 1.2rem;
}

.plandetail {
  color: #000;
  display: flex;
  flex-direction: column;
}

.plandetail .planrow {
  margin-bottom: 5px;
  font-size: 0.8rem;
}

.plandetail .planrow b {
  font-size: 1.2rem;
  margin-right: 15px;
  margin-bottom: 5px;
}

.planterms {
  color: #000;
  min-height: 100px;
}

.planterms .term {
  color: #000;
  margin-bottom: 8px;
  font-size: 0.8rem;
}

.footer {
  border-top: 1px solid #ccc;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 0px;
  margin-bottom: 10px;
}

.footer .whatyouget {
  color: #000;
  text-decoration: underline;
  font-size: 0.8rem;
}

.selectButton .btnSelect {
  background: #fff !important;
  padding: 10px 40px !important;
  border: none;
  color: #d134b4;
  box-shadow: 0px 0px 3px 0px #ccc;
  font-size: 13px;
  font-weight: bold;
  text-transform: capitalize;
}

.limitedOfferSection {
  color: #000;
}

.limitedTimeOffer {
  width: 100px;
  text-align: center;
  color: #000;
  font-size: 0.6rem;
  color: #fff;
  font-weight: bold;
  border-radius: 50px;
  background: #FF0099;
  /* fallback for old browsers */
  background: -webkit-linear-gradient(to right,
      #493240,
      #FF0099);
  /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to right,
      #5831a0,
      #cc0ead);
  /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
}

.limitedOfferSection .limitedTimeOfferText {
  color: #000;
  font-size: 0.8rem;
}

.cross {
  position: relative;
  display: inline-block;
  color: gray;
  font-size: 25px;
}

.cross::before,
.cross::after {
  content: '';
  width: 100%;
  position: absolute;
  right: 0;
  top: 50%;
}

.cross::before {
  border-bottom: 2px solid black;
  transform: skewY(23deg);
  -webkit-transform: skewY(23deg);
}

.font28 {
  font-size: 1.9rem !important
}

.most-popular {
  background:#00205b;
  color:white;
  position:absolute;
  top: -20px;
  z-index: 1000;
  font-weight: bold;
  font-size: 14px;
  padding-left: 15px;
  padding-right: 15px;
  margin-left: 5px;
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
}
</style>

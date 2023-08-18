<template>
    <div class="container">
        <h3 class="green text-center">How Eazipay Works</h3>
        <p class="grey text-center">Get started in 3 simple steps.</p>

        <div class="row my-5">

            <div class="col-lg-6 p-5">
                <div class="onboard-bg px-2">
                    <div class="gif" v-if="stage == 1" v-motion-pop>
                        <img src="../assets/images/step1.gif" class="img-fluid" alt="onboarding image">
                    </div>
                    <div class="gif" v-if="stage == 2">
                        <img src="../assets/images/step2.gif" class="img-fluid" alt="onboarding image" v-motion-pop>
                    </div>
                    <div class="gif" v-if="stage == 3">
                        <img src="../assets/images/step3.gif" class="img-fluid" alt="onboarding image" v-motion-pop>
                    </div>
                </div>
            </div>

            <div class="col-lg-6 p-5 desktop">

                <div class="step step1">
                    <div class="number" :class="{ 'active': stage === 1 }" @click="changeStage(1)">
                        <h3 class="num">1</h3>
                    </div>
                    <svg width="50" height="200" viewBox="0 0 50 222" fill="#D9EBCD" xmlns="http://www.w3.org/2000/svg">
                        <defs>
                            <linearGradient id="left-to-right">
                                <stop offset="0" stop-color="#11453B">
                                    <animate dur="10s" attributeName="offset" from="0" to="1" id="myLoop" />
                                </stop>
                                <stop offset="0" stop-color="#D9EBCD">
                                    <animate dur="10s" attributeName="offset" from="0" to="1" />
                                </stop>
                            </linearGradient>
                        </defs>
                        <path d="M27.9477 211C27.9477 216.891 32.7233 221.667 38.6144 221.667C44.5054 221.667 49.281 216.891 49.281 211C49.281 205.109 44.5054 200.333 38.6144 200.333C32.7233 200.333 27.9477 205.109 27.9477 211ZM38.6144 0H26.6144V4H38.6144V0ZM0.61438 26V187H4.61438V26H0.61438ZM26.6144 213H38.6144V209H26.6144V213ZM0.61438 187C0.61438 201.359 12.255 213 26.6144 213V209C14.4641 209 4.61438 199.15 4.61438 187H0.61438ZM26.6144 0C12.255 0 0.61438 11.6406 0.61438 26H4.61438C4.61438 13.8497 14.4641 4 26.6144 4V0Z" fill="url(#left-to-right)"/>
                        <mask id="mask0_2797_462" style="mask-type:alpha" maskUnits="userSpaceOnUse" x="0" y="0" width="50" height="222">
                        <path d="M27.9477 211C27.9477 216.891 32.7233 221.667 38.6144 221.667C44.5054 221.667 49.281 216.891 49.281 211C49.281 205.109 44.5054 200.333 38.6144 200.333C32.7233 200.333 27.9477 205.109 27.9477 211ZM38.6144 0H26.6144V4H38.6144V0ZM0.61438 26V187H4.61438V26H0.61438ZM26.6144 213H38.6144V209H26.6144V213ZM0.61438 187C0.61438 201.359 12.255 213 26.6144 213V209C14.4641 209 4.61438 199.15 4.61438 187H0.61438ZM26.6144 0C12.255 0 0.61438 11.6406 0.61438 26H4.61438C4.61438 13.8497 14.4641 4 26.6144 4V0Z" fill="#D9EBCD"/>
                        </mask>
                        <g mask="url(#mask0_2797_462)">
                        <rect x="47.6144" y="-6" width="5" height="13" fill="#11453B"/>
                        </g>
                    </svg>
                    <div class="ps-3 detail">
                        <h5 class="mb-2">Create your free account</h5>
                        <p class="grey">Click here to set up your Eazipay account.</p>
                    </div>
                </div>

                <div class="step step2">
                    <div class="number" :class="{ 'active': stage === 2 }" @click="changeStage(2)">
                        <h3 class="num">2</h3>
                    </div>
                    <svg width="302" height="245" viewBox="0 0 302 245" fill="#D9EBCD" xmlns="http://www.w3.org/2000/svg">
                        <defs>
                            <linearGradient id="green-fill">
                                <stop offset="0" stop-color="#11453B">
                                    <animate dur="4s" attributeName="offset" from="0" to="1" id="myLoop" />
                                </stop>
                                <stop offset="0" stop-color="#D9EBCD">
                                    <animate dur="4s" attributeName="offset" from="0" to="1" />
                                </stop>
                            </linearGradient>
                        </defs>
                        <path d="M22.281 234C22.281 239.891 17.5054 244.667 11.6144 244.667C5.72336 244.667 0.947723 239.891 0.947723 234C0.947723 228.109 5.72336 223.333 11.6144 223.333C17.5054 223.333 22.281 228.109 22.281 234ZM11.6144 0H275.614V4H11.6144V0ZM301.614 26V210H297.614V26H301.614ZM275.614 236H11.6144V232H275.614V236ZM301.614 210C301.614 224.359 289.974 236 275.614 236V232C287.765 232 297.614 222.15 297.614 210H301.614ZM275.614 0C289.974 0 301.614 11.6406 301.614 26H297.614C297.614 13.8497 287.765 4 275.614 4V0Z" fill="#url(green-fill)"/>
                        <mask id="mask0_2797_493" style="mask-type:alpha" maskUnits="userSpaceOnUse" x="0" y="0" width="302" height="245">
                        <path d="M22.281 234C22.281 239.891 17.5054 244.667 11.6144 244.667C5.72336 244.667 0.947723 239.891 0.947723 234C0.947723 228.109 5.72336 223.333 11.6144 223.333C17.5054 223.333 22.281 228.109 22.281 234ZM11.6144 0H275.614V4H11.6144V0ZM301.614 26V210H297.614V26H301.614ZM275.614 236H11.6144V232H275.614V236ZM301.614 210C301.614 224.359 289.974 236 275.614 236V232C287.765 232 297.614 222.15 297.614 210H301.614ZM275.614 0C289.974 0 301.614 11.6406 301.614 26H297.614C297.614 13.8497 287.765 4 275.614 4V0Z" fill="#D9EBCD"/>
                        </mask>
                        <g mask="url(#mask0_2797_493)">
                        </g>
                    </svg>
                    <div class="ps-3 detail">
                        <h5 class="mb-2">Add Employee Data</h5>
                        <p class="grey shorten">Your Employee information is 100% safe and secure.</p>
                    </div>
                </div>
                <div class="step step3">
                    <div class="number" :class="{ 'active': stage === 3 }" @click="changeStage(3)">
                        <h3 class="num">3</h3>
                    </div>
                    <div class="ps-3 detail">
                        <h5 class="mb-2">Prepare your transaction</h5>
                        <p class="grey shorten">Run payroll: Bulk Salaries and Compliance are done at once!</p>
                    </div>
                </div>

            </div>

            <div class="mobile text-center col-lg-6">
                <div class="stage-details">
                    <div class="stage1" v-if="stage === 1" v-motion-pop>
                        <div class="">
                            <h4 class="gold">step 1</h4>
                            <h5 class="mb-2 green ms-3">Create your free account</h5>
                        </div>
                        <p class="grey">Click here to set up your Eazipay account.</p>
                    </div>
                    <div class="stage2" v-if="stage === 2" v-motion-pop>
                        <div class="">
                            <h4 class="gold">step 2</h4>
                            <h5 class="mb-2 green ms-3">Add Employee Data</h5>
                        </div>
                        <p class="grey">Your Employee information is 100% safe and secure.</p>
                    </div>
                    <div class="stage3" v-if="stage === 3" v-motion-pop>
                        <div class="">
                            <h4 class="gold">step 3</h4>
                            <h5 class="mb-2 green ms-3">Prepare your transaction</h5>
                        </div>
                        <p class="grey">Run payroll: Bulk Salaries and Compliance are done at once!</p>
                    </div>
                </div>
                <div class="stages d-flex">
                    <div class="number mx-2" :class="{ 'active': stage === 1 }" @click="changeStage(1)">
                        <h3 class="num">1</h3>
                    </div>
                    <div class="number mx-2" :class="{ 'active': stage === 2 }" @click="changeStage(2)">
                        <h3 class="num">2</h3>
                    </div>
                    <div class="number mx-2" :class="{ 'active': stage === 3 }" @click="changeStage(3)">
                        <h3 class="num">3</h3>
                    </div>
                </div>
            </div>

        </div>
    </div>
</template>
<script>
export default {
    name: 'HowItWorks',
    data() {
        return {
            stage: 1
        }
    },
    mounted() {
        this.nextStage();
    },
    methods: {
        nextStage() {
            setInterval(() => {
                if (this.stage === 1) {
                    this.stage = 2;
                } else if (this.stage === 2) {
                    this.stage = 3;
                } else {
                    this.stage = 1;
                }
            }, 10000)
        },
        changeStage(number) {
            this.stage = number;
        }
    }
}
</script>
<style scoped>
h5 {
    font-family: 'Aeonik-Bold';
}
h3 {
    font-size: 2.3rem;
}
.onboard-bg {
    background-image: url(../assets/images/onboard-bg.png);
    background-repeat: no-repeat;
    background-size: contain;
    background-position: center center;
    display: flex;
    align-items: center;
    justify-content: center;
}
/* .onboard-bg img {
    width: 65%;
    border-radius: 56px;
} */
.gif {
    width: 65%;
}
.gif img {
    width: 100%;
    border-radius: 56px;
}
.step {
    position: relative;
}
.step svg {
    position: absolute;
}
.step1 {
    height: 190px;
}
.step2 {
    height: 235px;
}
.step2 svg {
    right: 4.5rem;
}
.detail {
    display: flex;
    flex-direction: column;
    padding-top: 4rem;
    margin-left: 3.125rem;
    justify-items: center;
}
div.number {
    width: 3rem;
    height: 3rem;
    background-color: #F2F1F1;
    color: #11453B;
    border-radius: 8px;
    display: flex;
    align-items: center;
    justify-content: center;
    position: absolute;
    left: 3.125rem;
    top: -1.5rem;
    transition: all 0.2s linear;
    cursor: pointer;
    z-index: 1;
}
.active {
    background-color: #11453B !important;
    color: #FFF !important;
}
h3.num {
    font-family: 'Aeonik-Bold';
    margin: 0;
    font-size: 2rem;
}
.shorten {
    width: 80%;
}
.mobile {
    display: none;
}
/* .gif {
    opacity: 1 !important;
    transform: scale(1) !important;
} */
@media(max-width: 1365px) {
    svg {
        display: none;
    }
    .step {
        box-shadow: 0px 20px 48px 0px rgba(170, 170, 170, 0.29);
        border-radius: 16px;
        margin-bottom: 2rem;
        padding: 3rem 1rem;
        height: auto;
    }
    .detail {
        margin: auto 1rem;
        padding-top: 0;
    }
}
@media (max-width: 992px) {
    .desktop {
        display: none;
    }
    .mobile {
        display:flex;
        flex-direction: column;
        align-items: center ;
    }
    div.number {
        position: relative;
        left: 0;
        top: 0;
        transform: scale(0.7);
    }
}
@media (max-width: 575px) {
    /* .onboard-bg img {
        border-radius: 32px;
    } */
    .gif img {
        border-radius: 32px;
    }
    .col-lg-6.p-5 {
        padding-top: 1rem !important;
    }
    h3 {
        font-size: 2rem;
    }
}
</style>
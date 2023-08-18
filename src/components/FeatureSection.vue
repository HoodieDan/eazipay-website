<template>
    <div class="bg-pattern">
        <img src="../assets/images/wave.png" class="wave" alt="wave">

        <div class="container text-center mt-5">
        <h2>For Individuals and Businesses</h2>
        <p class="grey mb-5">Join 200+ businesses using Eazipay's easy solution.</p>

        <div class="cards">

            <div class="green-card card1">
                <h3>Tamper-proof Payroll for Life</h3>

                <p>Your staff payroll history is kept in one place forever.</p>
                <p>No more excel sheet or manual records.</p>
                <p>Download your payroll history anytime you need it.</p>
            </div>

            <div class="green-card card2">
                <h3>All Payroll, Anytime Anywhere</h3>

                <p>Wherever you are, Eazipay has got you covered on ALL your Payroll tasks.</p>
                <p>Whether it is Taxes, Pension insurances HMOs, trustfunds, Eazipay handle all your compliances in one place and easily, in seconds!</p>
            </div>

            <div class="green-card card3">
                <h3>Payroll in Seconds</h3>

                <p>Never again will you spend more than 2 minutes on payroll.</p>
                <p>Just click on your staff and bulk-pay them at once.</p>
                <p>Payment is done permanently.</p>
            </div>

        </div>

        <div class="query">
            <p class="text-center">We are happy to answer your queries. Please, reach us at <a href="mailto:hi@eazypay.com" class="red"> hi@myeazipay.com </a> and expect our response shortly after.</p>
        </div>

    </div>
    </div>
</template>
<script>
export default {
    
}
</script>
<style scoped>
.bg-pattern {
    background-image: url('../assets/images/bg-pattern.png');
    position: relative;
}
.wave {
    z-index: -1;
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
}
.container {
    padding-top: 5rem;
    padding-bottom: 5rem;
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
}
h2 {
    font-size: 2.5rem;
    color: #11453B;
} 
h3 {
    font-family: 'Aeonik-Bold';
}
div.cards {
    position: relative;
}
.green-card {
    background: radial-gradient(50% 50% at 50% 50%,rgba(217,235,205,.14) 0,rgba(217,235,205,.0266) 100%),#11453b;
    box-shadow: 0 13px 20px hsla(0,0%,9%,.2), -11px 0 19px hsla(0,0%,9%,.3);
    color: #fff;
    padding: 3rem;
    transition: .45s cubic-bezier(.175,.585,.32,1.2075);
    height: 18.5rem;
    width: 45%;
    border-radius: 16px;
    position: absolute;
    text-align: left;
    transition: all 0.3s ease-out;
    cursor: pointer;
}
.card3 {
    z-index: 3;
    transform: translateX(40rem);
}
.card3:hover {
    transform: translateX(38rem);
}
.card2:hover + .card3 {
    transform: translateX(45rem);
}
.card2 {
    z-index: 2;
    transform: translateX(20rem);
}
.card2:hover {
    transform: translateX(15rem);
}
.card1:hover + .card2 {
    transform: translateX(25rem);
}
.card1:hover {
    transform: translateX(-5rem);
}
.query {
    display: flex;
    align-self: center;
    padding-top: 23rem;
    width: 70%;
}
@media (max-width: 1024px) {
    .green-card {
        width: 100%;
        position: relative;
        margin-bottom: 1.5rem;
        transform: translateX(0);
        height: auto;
    }
    .query {
        padding-top: 3rem;
    }
    .card3:hover {
        transform: translateX(0);
    }
    .card2:hover + .card3 {
        transform: translateX(0);
    }
    .card2:hover {
        transform: translateX(0);
    }
    .card1:hover + .card2 {
        transform: translateX(0);
    }
    .card1:hover {
        transform: translateX(-0);
    }
    .wave {
        display: none;
    }
}
@media (max-width: 992px) {
    .green-card {
        color: #11453B;
        background-color: #fff;
        box-shadow: 0px 20px 48px 0px rgba(170, 170, 170, 0.29);
        padding: 2rem 3rem;
    }
}
</style>
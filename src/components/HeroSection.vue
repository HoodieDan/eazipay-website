<template>
    <div class="hero-bg">
        <div class="container">
            <div class="row">
                <div class="col-lg-6">
                    <h1>Run your <span class="green">payroll</span> <span class="gold">easily</span> in <span class="red">seconds</span></h1>
                    <p class="mt-3 summary">
                        We’ve built an all-inclusive simple solution for individual and businesses to manage staff, pay salaries, bills, and relevant taxes all at once.
                    </p>
                    <button class="btn btn2 mt-2">start using free, forever</button>
                    <p class="mt-4">Download the Eazipay App</p>
                    <div class="download-links d-flex mt-2">
                        <img src="../assets/images/gplay.png" alt="google play download link" class="me-2">
                        <img src="../assets/images/appstore.png" alt="app store download link">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    
}
</script>
<style scoped>
p {
    color: #000;
}
h1 {
    font-family: 'Mellow-Bold';
    font-size: 4rem;
}
p.summary {
    color: #515251;
    width: 80%;
}
.btn2 {
  background-color: #11453B !important;
  border: #11453B 1px solid;
  color: #FFF;
  font-size: 1rem;
  padding: 0.8rem 3.5rem;
  border-radius: 24px;
  transition: all 0.5s linear;
}
.download-links img {
    width: 12rem;
    border-radius: 9px;
    box-shadow: 0px 20px 48px 0px rgba(170, 170, 170, 0.29);
    cursor: pointer;
}
.btn:hover,
.download-links img:hover {
  animation: bounce 1s ease-in-out forwards;
}
@media (min-width: 1024px) {
    .hero-bg {
        height: 35rem;
        background-image: url(../assets/images/hero.png);
        background-position: 100%;
        background-repeat: no-repeat;
        background-size: auto 100%;
        display: flex;
        align-items: center;
    }
}
@media (max-width: 1023px) {
    .col-lg-6 {
        width: 100%;
        max-width: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    .col-lg-6 > * {
        text-align: center !important;
    }
    .download-links {
        justify-content: center;
    }
}
@media (max-width: 575px) {
    h1 {
        font-size: 3rem;
    }
    .download-links img {
        width: 8rem;
    }
}
</style>
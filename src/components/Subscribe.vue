<template>
    <div class="pattern-bg">

        <div class="container p-5">
            <div class="row">
                <div class="col-lg-6 p-3">
                    <img src="../assets/images/sub-dots.png" class="sub-dots" alt="dots">

                    <h2 class="mt-5">Free forever for your <span class="red">salary payment</span></h2>
                    <p class="grey mt-3 mb-3">Subscribe to the easy life today.</p>
                    <div class="download-links d-flex mt-3 mb-5">
                        <img src="../assets/images/gplay.png" alt="google play download link" class="me-2 img-fluid">
                        <img src="../assets/images/appstore.png" alt="app store download link" class="img-fluid">
                    </div>
                </div>
                <div class="col-lg-6 p-5 sub-div">
                    <img src="../assets/images/sub.png" class="img-fluid sub" alt="subscribe">
                </div>
            </div>
        </div>

    </div>
</template>

<script>
export default {
    name: 'Subscription',
    data() {
        return {

        }
    }
}
</script>

<style scoped>
h2 {
    font-size: 3rem;
    padding-top: 3rem;
}
.pattern-bg {
  background-color: #ffe9e7;
  background-image: url('../assets/images/bg-pattern.png');
  background-size: cover;
  background-position: 50%;
  position: relative;
}
.download-links img {
    width: 12rem;
    border-radius: 9px;
    box-shadow: 0px 20px 48px 0px rgba(170, 170, 170, 0.29);
}
.sub-dots {
    position: absolute;
    top: 0;
    left: 1rem;
}
@media (max-width: 992px) {
    .col-lg-6 {
        text-align: center;
    }
    .download-links {
        justify-content: center;
    }
}
@media (max-width: 575px) {
    .download-links img {
        width: 8rem;
    }
    .sub-div {
        padding: 1rem !important;
    }
    .container {
        padding: 1.5rem !important;
    }
}
</style>
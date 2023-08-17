<template>
    <div>
        <div class="footer-middle py-5">
            <div class="container">
                <div class="row">
                    <div class="col-lg-4 company-info">
                        <div>
                            <img src="../assets/images/logo.svg" alt="logo" class="me-4 img-fluid logo">
                        </div>

                        <div class="company-address">
                            <p>Copyright © 2023 Eazipay.</p>
                            <p>All Rights Reserved.</p>
                        </div>

                        <div class="social-networks">
                            <img src="../assets/images/instagram.png" class="me-4" alt="instagram logo">
                            <img src="../assets/images/twitter.png" class="me-4" alt="twitter logo">
                            <img src="../assets/images/linkedin.png" class="me-4" alt="linkedin logo">
                            <img src="../assets/images/facebook.png" class="me-4" alt="facebook logo">
                        </div>
                    </div>
                    <div class="col-lg-2 col-md-3 col-sm-3 col-6 flex-col">
                        <h4 class="mb-3">PRODUCT</h4>
                        <router-link to="#" class="link">Individual</router-link>
                        <router-link to="#" class="link">Businesses</router-link>
                        <router-link to="#" class="link">Request Demo</router-link>
                        <router-link to="#" class="link">Pricing</router-link>
                    </div>
                    <div class="col-lg-2 col-md-3 col-sm-3 col-6 flex-col">
                        <h4 class="mb-3">Legal</h4>
                        <router-link to="#" class="link">Privacy Policy</router-link>
                        <router-link to="#" class="link">Terms of Service</router-link>
                    </div>
                    <div class="col-lg-2 col-md-3 col-sm-3 col-6 flex-col">
                        <h4 class="mb-3">Resources</h4>
                        <router-link to="#" class="link">FAQs</router-link>
                        <router-link to="#" class="link">Blog</router-link>
                        <router-link to="#" class="link">Career</router-link>
                        <router-link to="#" class="link">Customer Stories</router-link>
                    </div>
                    <div class="col-lg-2 col-md-3 col-sm-3 col-6 flex-col">
                        <h4 class="mb-3">Contact Us</h4>
                        <router-link to="#" class="link">Eazipay@gmail.com</router-link>
                        <router-link to="#" class="link">+234 816 878 9518</router-link>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'FootingSection',

}
</script>

<style scoped>
h2 {
    font-weight: 500;
    font-size: 3rem;
}
h4 {
    font-family: 'Aeonik-Bold';
    font-size: 1.2rem;
}
p {
    color: #7C7C7C;
}
.logo {
    width: 8rem;
}
.btn {
    border-radius: 32px;
    background-color: #3c0000;
    color: #000;
    border: none;
    padding: 1rem 9rem;
}
.btn:hover {
    background-color: #360000;
}
.img-fluid {
    height: 3rem;
    position: relative;
    bottom: .5rem;
}
.link {
    font-size: 0.8rem;
    color: #7C7C7C;
    margin-bottom: 1rem;
    transform: all 0.3s ease-in-out;
    cursor: pointer;
}
.link:hover {
    color: #11453B;
}
.company-address {
    font-size: 0.8rem;
}
a {
    color: #000;
}
.company-email {
    font-size: 0.8rem;
    color: #000;
    text-decoration: underline;
    padding-bottom: 0.3rem;
}
.company-info {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}
.link:before {
    background: #fff;
}
.flex-col {
    display: flex;
    flex-direction: column;
}
@media (max-width: 992px) {
    .company-info {
        margin-bottom: 4rem;
    }
    h4, .company-address, .company-email {
        margin-bottom: 2rem;
    }
    h2 {
        text-align: center;
        margin-bottom: 2rem;
    }
}
@media (max-width: 575px) {
    .btn {
        padding: 1rem;
    }
}
</style>
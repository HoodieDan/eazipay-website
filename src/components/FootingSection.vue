<template>
    <div>
        <div class="footer py-5">
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
                            <img src="../assets/images/Instagram.png" class="me-4" alt="instagram logo">
                            <img src="../assets/images/Twitter.png" class="me-4" alt="twitter logo">
                            <img src="../assets/images/linkedin.png" class="me-4" alt="linkedin logo">
                            <img src="../assets/images/facebook.png" class="me-4" alt="facebook logo">
                        </div>
                    </div>
                    <div class="col-lg-2 col-md-3 col-sm-3 col-6 flex-col">
                        <h4 class="mb-3">Product</h4>
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
                        <a href="mailto:eazipay@gmail.com" class="link">eazipay@gmail.com</a>
                        <a href="tel:+234 816 878 9518" class="link">+234 816 878 9518</a>
                        <div class="d-flex email">
                            <input class="text-field mb-3 mx-0" type="text" name="email" placeholder="Your email address">
                            <i class="fa-regular fa-paper-plane"></i>
                        </div>
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
.footer {
    border-top: #EAEAEA 1px solid;
}
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
    transition: all 0.4s ease-out;
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
input.text-field {
  width: 100%;
  border: none;
  border-radius: 16px;
  /* height: 2.3rem; */
  background-color: #F2F1F1;
  font-size: 0.7rem;
  padding: 0.5rem 2rem 0.5rem 1rem;
  color: #11453B;
}
input::placeholder {
  color: #515251;
}
input:focus,
input:active {
  outline-color: #11453B;
}
.fa-regular {
    z-index: 2;
    position: relative;
    top: 0.6rem;
    right: 1.7rem;
    color: #515251;
    transition: all 0.7s ease-in-out;
    cursor: pointer;
}
.fa-regular:hover {
    transform: rotateZ(10deg);
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
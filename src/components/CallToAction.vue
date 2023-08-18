<template>
    <div class="cta">
        <img src="../assets/images/cta-dots.png" class="cta-dots" alt="dots">
        <div class="container">
            <div class="row mt-3 mb-3">
                    <div class="col-lg-6 p-5 left">
                        <div class="p-3 get">
                            <h2 class="green">Get an Exclusive Demo of Eazipay</h2>
                            <p class="mt-2 deet">Our greatest priority is to put you and your business first. Let’s show you how we can help.</p>
                        </div>
                    </div>

                    <div class="col-lg-6 p-3 right">
                        <div class="about-card text-center">
                            <h4>First things first.</h4>
                            <p class="grey">We want to serve you better. Tell us a bit about yourself and your company.</p>

                            <div class="row menu p-1">
                                <div class="col-6">
                                    <button class="individual btn menu-button me-1" :class="{ 'active': tab === 'individual' }" @click="switchTab('individual')">
                                        Individual
                                    </button>
                                </div>
                                <div class="col-6 pe-1">
                                    <button class="company btn menu-button mx-1" :class="{ 'active': tab === 'company' }" @click="switchTab('company')">
                                        Company
                                    </button>
                                </div>
                            </div>

                            <form action="/" class="mt-3 mb-3">
                                <div class="item">
                                    <!-- <label for="firstName">First Name:</label> <br> -->
                                    <input class="text-field mb-3 mx-0" type="text" name="firstName" placeholder="First Name">
                                </div>
                                <div class="item">
                                    <!-- <label for="lastName">Last Name:</label> <br> -->
                                    <input class="text-field mb-3" type="text" name="lastName" placeholder="Last Name">
                                </div>
                                <div class="item">
                                    <!-- <label for="email">Email Address:</label> <br> -->
                                    <input class="text-field mb-3" type="email" name="email" placeholder="Email">
                                </div>
                                <div class="item">
                                    <!-- <label for="phoneNo">Phone Number:</label> <br> -->
                                    <input class="text-field mb-3" type="text" name="jobTitle" placeholder="Job Title">
                                </div>
                                <div class="item">
                                    <!-- <label for="phoneNo">Phone Number:</label> <br> -->
                                    <input class="text-field mb-3" type="text" name="companySize" placeholder="Company Size">
                                </div>
                            </form>

                            <button class="btn menu-button active demo w-100">
                                Request Demo
                            </button>
                        </div>
                    </div>
            </div> 
        </div>
    </div>
</template>
<script>
export default {
    name: 'CallToAction',
    data() {
        return {
            tab: 'individual',
        }
    },
    methods: {
        switchTab(tab) {
            this.tab = tab;
        }
    }
}
</script>
<style scoped>
div.cta {
    position: relative;
}
h2 {
    font-size: 3rem;
} 
h4 {
    font-family: 'Aeonik-Bold';
}
p.deet {
    width: 80%;
}
div.left {
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
}
div.right {
    display: flex;
    flex-direction: column;
    align-items: center;
}
.cta-dots {
    position: absolute;
    z-index: -1;
    left: 0;
    top: 0.5rem;
}
.about-card {
    box-shadow: 0px 20px 48px 0px rgba(170, 170, 170, 0.29);
    padding: 2rem 3rem;
    border-radius: 8px;
}
.menu {
    border: 1px solid #E7E8E7;
    border-radius: 8px;
    max-width: 100%;
    margin-left: 0;
}
.col-6 {
    padding: 0;
}
.menu-button {
    width: 100%;
    border-radius: 8px;
    border: 1px solid #E7E8E7;
    color: #515251;
    background-color: #f2f1f1;
}
.menu-button:active, .menu-button:focus {
    outline: none;
}
.active {
    background-color: #11453B;
    color: #FFF;
}
input.text-field {
  width: 100%;
  border: #B5B6B5 1px solid;
  border-radius: 16px;
  height: 2.3rem;
  padding: 0.5rem 1.5rem;
  color: #11453B;
}
input::placeholder {
  color: #B5B6B5;
}
input:focus,
input:active {
  outline-color: #11453B;
}
.demo {
    border-radius: 32px;
}
@media (max-width: 992px) {
    .cta-dots {
        top: -5rem;
    }
    .left {
        text-align: center;
    }
    .get {
        display: flex;
        flex-direction: column;
        align-items: center;
    }
}
@media (max-width: 768px) {
    .left {
        padding: 3rem 2rem 1rem !important;
    }
    .about-card {
        border-radius: 16px;
    }
}
</style>
<template>
    <div class="cta">
        <img src="../assets/images/cta-dots.png" class="cta-dots" alt="dots">
        <div class="container">
            <div class="row">
                    <div class="col-lg-6 p-5 left">
                        <div class="p-5">
                            <h2 class="green">Get an Exclusive Demo of Eazipay</h2>
                            <p class="mt-2 deet">Our greatest priority is to put you and your business first. Let’s show you how we can help.</p>
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
div.cta {
    position: relative;
}
h2 {
    font-size: 3rem;
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
.cta-dots {
    position: absolute;
    z-index: -1;
    left: 0;
    top: 3rem;
}
</style>
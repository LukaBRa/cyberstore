<script setup>



</script>

<template>

<footer>
    <div class="container">

        <div class="row">

            <div class="footer-card col-lg-4 col-12">
                <div class="icon">
                    <i class="fa-solid fa-headset"></i>
                </div>
                <div class="footer-card-info">
                    <p class="footer-card-title">Call Center</p>
                    <a class="footer-card-link" href="tel:(+381)866-540-3229">(+381)866-540-3229</a>
                </div>
            </div>

            <div class="footer-card col-lg-4 col-12">
                <div class="icon">
                    <i class="fa-solid fa-cart-flatbed-suitcase"></i>
                </div>
                <div class="footer-card-info">
                    <p class="footer-card-title">Free Delivery</p>
                    <p class="footer-card-paragraph">Free delivery on the territory of SRB for all amounts over $100</p>
                </div>
            </div>
            <div class="footer-card col-lg-4 col-12">
                <div class="icon">
                    <i class="fa-solid fa-tags"></i>
                </div>
                <div class="footer-card-info">
                    <p class="footer-card-title">Gift Cards</p>
                    <a class="footer-card-link" href="">SAVE UP TO 20%</a>
                </div>
            </div>

        </div>

        <div class="row">
            <div class="col-lg-3 col-12">
                <p class="footer-link-group-title">Get to Know Us</p>
                <div class="footer-link-group">
                    <a href="" class="footer-link">About us</a>
                    <a href="" class="footer-link">Our Services</a>
                    <a href="" class="footer-link">Stores</a>
                    <a href="" class="footer-link">Contact Us</a>
                    <a href="" class="footer-link">Order Tracking</a>
                </div>
            </div>
            <div class="col-lg-3 col-12">
                <p class="footer-link-group-title">Customer Service</p>
                <div class="footer-link-group">
                    <a href="" class="footer-link">My account</a>
                    <a href="" class="footer-link">Order Tracking</a>
                    <a href="" class="footer-link">Pricing Plans</a>
                    <a href="" class="footer-link">Terms & Conditions</a>
                    <a href="" class="footer-link">Our Team</a>
                    <a href="" class="footer-link">FAQ</a>
                </div>
            </div>
            <div class="col-lg-3 col-12">
                <p class="footer-link-group-title">Quick Links</p>
                <div class="footer-link-group">
                    <a href="" class="footer-link">Smartphones</a>
                    <a href="" class="footer-link">Headphones</a>
                    <a href="" class="footer-link">Laptop & Tablets</a>
                    <a href="" class="footer-link">Gadgets</a>
                </div>
            </div>
            <div class="col-lg-3 col-12">
                <p class="footer-link-group-title">Sign up to Newsletter</p>
                <div class="subscription-div">
                    <input type="text" placeholder="Your Email Adress...">
                    <button class="subscribe-btn"><i class="fa-regular fa-paper-plane"></i></button>
                </div>
                <p class="footer-paragraph">Stay up to date with all the actions that we are saved for all our customers.</p>
                <div class="socials">
                    <a href="" class="footer-social"><i class="fa-brands fa-facebook-f"></i></a>
                    <a href="" class="footer-social"><i class="fa-brands fa-instagram"></i></a>
                    <a href="" class="footer-social"><i class="fa-brands fa-twitter"></i></a>
                    <a href="" class="footer-social"><i class="fa-brands fa-linkedin-in"></i></a>
                </div>
            </div>
        </div>

        <hr>

        <p class="copyright">&copy 2021 CyberStore, All Rights Reserved</p>

    </div>
</footer>

</template>

<style>

footer{
    background-color: var(--dark);
    margin-top: 5rem;
    padding: 2rem;
}

.footer-card{
    background-color: rgb(54, 54, 54);
    display: flex;
    align-items: center;
    gap: 1rem;
    border-right: 2px solid var(--dark);
    padding: 1rem;
}

.icon{
    color: white;
    font-size: 3rem;
}

.footer-card-title{
    color: white;
    font-size: 1.5rem;
}

.footer-card-info{
    color: white;
}

.footer-card-link{
    color: var(--blue);
    text-decoration: none;
    font-size: 1.5rem;
}

.footer-card-link:hover{
    text-decoration: underline;
}

.footer-link-group-title{
    color: white;
    margin-top: 2rem;
    font-size: 1.1rem;
    font-weight: bold;
}

.footer-link-group{
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
}

.footer-link{
    text-decoration: none;
    color: white;
    font-size: 0.9rem;
    transition: all 0.3s ease;
}

.footer-link:hover{
    color: var(--blue);
}

.subscription-div{
    border: 1px solid var(--blue);
    width: max-content;
}

.subscription-div input{
    padding: 0.5rem;
    background: none;
    border: none;
    color: white;
}

.subscription-div input::placeholder{
    color: white;
}

.subscription-div input:focus{
    outline: none;
}

.subscribe-btn{
    background-color: var(--blue);
    color: white;
    padding: 0.5rem;
    border: 1px solid var(--blue);
}

.footer-paragraph{
    color: white;
    margin-top: 1rem;
}

.socials{
    display: flex;
    gap: 1rem;
}

.footer-social{
    color: white;
    transition: all 0.3s ease;
}

.footer-social:hover{
    color: var(--blue);
}

hr{
    color: white;
}

.copyright{
    color: white;
    text-align: center;
}

</style>
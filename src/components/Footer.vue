<template>
    <footer class=" bg-footer text-white">
        <section class="lg:px-20 sm:px-14 px-8 py-14 flex lg:flex-row flex-col gap-20 border-b-8 border-secondary">
            <aside class=" md:basis-2/5 ">
                <h1 class="text-3xl font-semibold mb-8">Join our weekly digest!</h1>
                <p class="text-lg ">Get exclusive promotions & updates straight to your inbox.</p>
                <div class="my-12 flex">
                    <input type="email" placeholder="Enter your email..... " class="w-50 px-5 py-2 bg-black rounded-full border-0 outline-0">
                    <button class="bg-black px-4 py-2 ml-auto rounded-full border-none text-white cursor-pointer">Subscribe</button>
                </div>
                <button class="bg-primary px-4 py-2 rounded-full border-none text-white cursor-pointer">Create Free Store</button>
            </aside>
            <article class="md:basis-3/5 flex flex-row justify-between text-xs sm:text-base">
                <ul>
                    <li>FEATURES</li>
                    <li>Build Store</li>
                    <li>Sell NFT</li>
                    <li>Grow Business</li>
                </ul>
                <ul>
                    <li>SERVICES</li>
                    <li>Concierge</li>
                    <li>Customization</li>
                </ul>
                <ul>
                    <li>PRODUCT</li>
                    <li>About Us</li>
                    <li>Whitepaper</li>
                    <li>$N1 Token</li>
                    <li>Directory</li>
                </ul>
                <ul>
                    <li>RESOURCES</li>
                    <li>Help Center</li>
                    <li>NFTify Branding</li>
                    <li>Success Stories</li>
                    <li>Video Tutorials</li>
                    <li>RESOURCES</li>
                    <li>Contact Support</li>
                </ul>
            </article>
        </section>
        <Copyright />
    </footer>
</template>
  
  
<script>
import Copyright from './Copyright.vue';
export default {  
    components:{
        Copyright
    }
  }


  
</script>
  
<style scoped>
    .bg-footer{
        width: 100%;
        height: 100%;
        background: linear-gradient(180deg, #52057B, #000000);
    }
    input{
        width: 70%;
    }
    article ul li:nth-child(1){
        font-weight: 900;
    }
    li{
        margin-bottom: 1.5rem;
    }
</style>
  
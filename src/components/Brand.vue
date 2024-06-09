<template>
    <section class="bg-secondary text-white">
        <div class="lg:px-20 sm:px-14 px-8 py-4 flex flex-col md:flex-row items-center justify-between ">
            <div class="  md:basis-1/3 flex ">
                <p class="text-2xl">Powering leading brands</p>
            </div>
            <div class=" md:basis-1/3 flex justify-center my-10 md:my-0">
                <img src="../../public/Images/Frame 6.png" alt="">
            </div>
            <!-- <div class=" md:basis-1/3 flex justify-center my-10 md:my-0">
                <div class=" relative coindesk w-7">
                    <span></span>
                    <span></span>
                    <span></span>
                    <span></span>
                    <span></span>
                    <span></span>
                    <span></span>
                    <span></span>
                    <span></span>
                </div>
                <p class="text-lg font-bold ml-3">Coindesk</p>
            </div> -->
            <div class=" md:basis-1/3 justify-end flex">
                <img src="../../public/Images/Frame 8.png" alt="">
            </div>
            <!-- <div class=" md:basis-1/3 justify-end flex">
                <div class=" relative heftyverse w-10">
                    <span></span>
                    <span></span>
                    <span></span>
                </div>
                <p class="text-lg font-bold ml-3">H E F T Y V E R S E</p>
            </div> -->
        </div>
    </section>
</template>


<script>
</script>
  
  <style scoped>
    .coindesk span{
        position: absolute;
        border: 4px solid white;
        border-radius: 100%;
    }
    .coindesk span:nth-child(1){
        right: 0px;
    }
    .coindesk span:nth-child(1)::before{
        position: absolute;
        content: " ";
        height: 3.8px;
        width: 7px;
        top: -2px;
        right: 1px;
        background: white;
    }
    .coindesk span:nth-child(2){
        left: 10px;
    }
    .coindesk span:nth-child(2)::before{
        position: absolute;
        content: " ";
        height: 3.8px;
        width: 7px;
        top: -2px;
        right: 1px;
        background: white;
    }
    .coindesk span:nth-child(3){
        left: 0px;
    }
    .coindesk span:nth-child(3)::before{
        position: absolute;
        content: " ";
        height: 7px;
        width: 3.8px;
        top: 1px;
        right: -0.9px;
        background: white;
    }
    .coindesk span:nth-child(4){
        top:10px
    }
    .coindesk span:nth-child(4)::before{
        position: absolute;
        content: " ";
        height: 7px;
        width: 3.8px;
        top: 1px;
        right: -0.9px;
        background: white;
    }
    .coindesk span:nth-child(5){
        bottom: 0;
    }
    .coindesk span:nth-child(5)::before{
        position: absolute;
        content: " ";
        height: 3.8px;
        width: 7px;
        top: -2px;
        right: -7px;
        background: white;
    }
    .coindesk span:nth-child(6){
        bottom: 0;
        left: 10px;
    }
    .coindesk span:nth-child(7){
        bottom: 2px;
        right: 1px;
        border: 2px solid white;
    }
    .coindesk span:nth-child(8){
        top: 12px;
        right: 1px;
        border: 2px solid white;
    }
    .coindesk span:nth-child(9){
        top: 12px;
        right: 11px;
        border: 2px solid white;
    }
    /* heftyverse */
    .heftyverse span{
        position: absolute;
        /* border: 4px solid white; */
        /* border-radius: 100%; */
    }
    .heftyverse span:nth-child(1){
        width: 16px;
        height: 11px;
        background-color: white;
    }
    .heftyverse span:nth-child(2){
        width: 16px;
        height: 11px;
        background-color: white;
        bottom: 0;
    }
    .heftyverse span:nth-child(3){
        width: 16px;
        height: 28px;
        background-color: white;
        right: 2px;
    }
    .heftyverse span:nth-child(3)::before{
        position: absolute;
        content: " ";
        width: 5.87px;
        height: 45.13px;
        /* bottom: -8px; */
        top: -6px;
        right: 7px;
        transform: rotate(34.11deg);
        background-color: #816797;   
    }
  </style>
  
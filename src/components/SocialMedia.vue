<template>
    <section class="social">
        <h1>Let's get to know each other better?</h1>
        <div class="media_content">
            <div class="media_content_block">
                <a  class="media" href="https://minter.ton.org/jetton/EQDf84FT8tdHZeI2-LXdb8gPMRqHRSABrmi8jI7MzvVpGJKZ" target="_blank"><div>
                    <img src="https://minter.ton.org/static/media/logo.3c3503cfcef8632dbe566c16c3921262.svg" alt="social logo">
                    <p>Minter</p>
                </div></a>
                <a class="media tonviewer" href="https://tonviewer.com/EQDf84FT8tdHZeI2-LXdb8gPMRqHRSABrmi8jI7MzvVpGJKZ" target="_blank"><div>
                    <!-- <img src="https://trader-otzyv.ru/wp-content/uploads/2023/07/tonviewer-225x227.jpg.webp" alt="social logo"> -->
                    <p>Tonviewer</p>
                </div></a>
                <a class="media" href="https://t.me/OpenCoinCommunity" target="_blank"><div >
                    <img src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Flogospng.org%2Fdownload%2Ftelegram%2Flogo-telegram-4096.png&f=1&nofb=1&ipt=b46a1b53ae161752773e3688777f925ce0585c66e29f58b13cc759305d97ec6d&ipo=images" alt="social logo">
                    <p>Telegram</p>
                </div></a>
            </div>
            <div class="media_content_block">
                <a class="media dedust" href="https://dedust.io/swap/TON/EQDf84FT8tdHZeI2-LXdb8gPMRqHRSABrmi8jI7MzvVpGJKZ" target="_blank"><div>
                    <img src="https://opencoin.fun/static/images/dedust.jpg" alt="social logo">
                    <p>DeDust swap</p>
                </div></a>
                <a class="media" href="https://dyor.io/ru/token/EQDf84FT8tdHZeI2-LXdb8gPMRqHRSABrmi8jI7MzvVpGJKZ" target="_blank"><div >
                    <img src="https://opencoin.fun/static/images/dyor.jpg" alt="social logo">
                    <p>dyor.io</p>
                </div></a>
            </div>
            
        </div>
    </section>
</template>
<script>
export default {
  
}
</script>
<style lang="scss" scoped>
* {
    margin: 0;
    padding: 0;
    color: black;
    box-sizing: border-box;
}
section{
    width: 100%;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin: 0 auto;
}
section h1{
    /* font-size: 80px; */
    display: block;
    width: 95%;
    text-align: center;
    margin: 0 auto;
    font-size: 70px;
    font-weight: 900;
    font-family: 'Kanit', sans-serif;
    
    @media screen and (max-width: 1024px) {
        font-size: 60px;
    }
    @media screen and (max-width: 768px) {
        font-size: 50px;
    }
    @media screen and (max-width: 500px) {
        font-size: 40px;
    }
}
.social {
    margin-bottom: 100px;
}
.media_content{
    margin: 60px 0 50px;
    width: 100%;
}
.media_content_block{
    display: flex;
    justify-content: center;
    width: 100%;
    
}
.media{
    width: 150px;
    height: 150px;
    background: #000000;
    margin: 10px 10px;
    border-radius: 15px;
    cursor: pointer;
    position: relative;
    display: flex;
    justify-content: center;
    /* text-align: center; */
   
    @media screen and (max-width: 1024px) {
        width: 120px;
        height: 120px;
        margin: 10px 5px;
        img {
            height: 60px;
            margin-top: 10px; 
        }
        svg {
            height: 60px;
            margin-top: 10px;
        }
        p{
            margin-bottom: 10px; 
            
        }
    }
    @media screen and (max-width: 768px) {
        font-size: 50px;
    }
    @media screen and (max-width: 500px) {
        font-size: 40px;
        width: 95%;
    }
}
.media img{
    margin: 20px auto 0;
    height: 70px;
    width: auto;
    border-radius: 10px;
    overflow: hidden;
}
.media {
    div {
        display: flex;
        flex-direction: column;
    }
}
.media svg{
    margin: 20px auto 0;
    height: 70px;
    width: auto;
    height: auto;
}
.media p{
    text-align: center;
    margin-top: 20px;
    color: #ffffff;
    font-size: 16px;
    margin-bottom: 20px;
    font-family: 'Kanit', sans-serif;
}
.tonviewer {
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>
<template>
    <section class="roadmap">
        <h1>Road Map</h1>
        <div class="roadmap_content">
            <div class="roadmap_content_block">
                <div class="roadmap_content_head">
                    <img src="https://opencoin.fun/static/images/wallet.png" alt="logo">
                    <h2>OpenWallet</h2>
                </div>
                <p>non-custodial web wallet for storing OpenCoin</p>
                <span class="tag">First need</span>
            </div>
            <div class="roadmap_content_block">
                <div class="roadmap_content_head">
                    <img src="https://opencoin.fun/static/images/pic1.png" alt="logo">
                    <h2>OpenCoin<br>marketplace</h2>
                </div>
                <p>Marketplace for buying and selling digital goods for OpenCoin</p>
                <span class="tag">soon</span>
            </div>
            <div class="roadmap_content_block">
                <div class="roadmap_content_head">
                    <img src="../connect.png" alt="logo">
                    <h2>OpenConnect<br>System</h2>
                </div>
                <p>Connection and payment system based on OpenCoin</p>
                <span class="tag">soon</span>
            </div>
            
        </div>
    </section>
</template>
<script>
export default {
  
}
</script>
<style scoped>
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
    font-family: 'Kanit', sans-serif;
    font-size: calc(70px + 24 * (100vw / 1920));
    font-weight: 900;
    margin: 0 auto;
    text-align: center;
    @media screen and (max-width: 1024px) {
        font-size: 60px;
    }
    @media screen and (max-width: 768px) {
        font-size: 50px;
    }
    @media screen and (max-width: 500px) {
        font-size: 40px;
        width: 95%;
    }
}
.roadmap_content{
    display: flex;
    margin: 50px 0px;
    @media screen and (max-width: 1024px) {
        flex-direction: column;
    }
}
.roadmap_content_block{
    width: 400px;
    
    margin: 15px;
    /* height: 260px; */
    background: rgb(240, 240, 240);
    border-radius: 20px;
    margin: 50px 15px;
    position: relative;
    text-align: left;
    padding: 20px;
    transition: 1.5s ease;
    cursor: pointer;

    @media screen and (max-width: 1324px) {
        width: 300px;
        margin: 15px 10px;
        h2{
            font-size: 25px;
            font-family: 'Kanit', sans-serif;
        }
    }
    @media screen and (max-width: 1024px) {
        width: 460px;
        margin: 15px 10px;
        h2{
            font-size: 25px;
            font-family: 'Kanit', sans-serif;
        }
    }
    
    @media screen and (max-width: 768px) {
        width: 320px;
        h2{
            font-size: 22px;
            font-family: 'Kanit', sans-serif;
        }
        .roadmap_content_head{
            display: flex;
            align-items: center;
            h2{
                margin-left: 20px;
                font-family: 'Kanit', sans-serif;
            }
        }
    }
   

}
.roadmap_content_block:hover {
    transform: scale(1.15);
    border: 2px solid #000000;
    z-index: 10;
}
.roadmap_content_block:hover h2 {
    color: #000000;
}
.roadmap_content_block:hover .tag {
    background: #000000;
}

.roadmap_content_block:hover p {
    font-family: 'Kanit', sans-serif;
    color: #000000;
}

.roadmap_content_block:hover img {
    filter: blur(0px);
}
.roadmap_content_block img{
    height: 60px;
    max-width: 65px;
    filter:blur(1px);
}
.roadmap_content_block h2{
    transition: 1.5s ease;
    font-family: 'Kanit', sans-serif;
    font-size: 30px;
    font-weight: 900;
    margin: 10px 0 15px;
    color: lightgray;
}
.roadmap_content_block p{
    transition: 1.5s ease;
    font-family: 'Kanit', sans-serif;
    margin-bottom: 40px;
    color: lightgray;
}
.roadmap_content_block .tag{
    transition: 1.5s ease;
    font-family: 'Kanit', sans-serif;
    background: lightgray;
    color: #ffffff;
    padding: 5px 10px;
    border-radius: 20px;
    position: absolute;
    bottom: 10px;
    left: 20px;
    box-sizing: border-box;

}
.roadmap_content_block .tag::before {
    content: "#";
}
</style>
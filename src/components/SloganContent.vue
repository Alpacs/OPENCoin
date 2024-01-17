<template>

    <div class="slogan-wrapper">
        <div class="slogan-block">
            <h1>Open coin for open<br><span class="text"></span></h1>
            <div class="logo-block">
                <svg id="_Слой_1" data-name="Слой 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1024 1024">
                    <circle class="cls-1" cx="511.57" cy="514.25" r="237"/>
                    <g>
                        <rect x="521.63" y="232.7" width="50" height="627.91" rx="10.21" ry="10.21" transform="translate(546.65 -226.41) rotate(45)"/>
                        <rect x="452.49" y="164.65" width="50" height="627.91" rx="10.21" ry="10.21" transform="translate(478.28 -197.46) rotate(45)"/>
                    </g>
                </svg>
                <span @click="goToInfo()" class="to-the-info"></span>
            </div>
        </div>
    </div>

</template>

<script>
import Typed from 'typed.js';

export default {

    name: 'SloganContent',
    data() {
        return {
            accent_word: ''
        }
    },
    methods: {
        goToInfo() {
            document.getElementById("info").scrollIntoView({ behavior: "smooth" });
            let button = document.querySelectorAll('.button')
            button.forEach(function(button) {
                button.addEventListener('touchstart', function() {
                button.classList.remove('hover');
                });
            });
        }
    },
    mounted() { 
        // 'ambitious|you|community|projects|people
        
        // eslint-disable-next-line no-unused-vars
        let typing = new Typed(".text", {
            strings: [
            'ambitious',
            'you'
            ,'community'
            ,'projects'
            ,'people'
            ],
            typeSpeed: 90,
            backSpeed: 50,
            loop: true,
            backDelay: 2000

        })
    }
}

</script>

<style scoped lang="scss">

    .slogan-wrapper {
        padding-top: 150px;
        box-sizing: border-box;
        height: 87vh;
        .slogan-block {
            height: 87vh;
            .logo-block {
                height: 60vh;
                display: flex;
                flex-direction: column;
                justify-content: space-between;
                align-items: center;
            }
            h1 {
                text-align: center;
                font-family: 'Kanit', sans-serif;
                font-size: 68px; 
                font-weight: 700;
                letter-spacing: 2px;
                .typed-cursor {
                    color: rgb(94, 171, 254);
                }
                span {
                    letter-spacing: 1px;
                }
            }
            img {
                display: block;
                margin: -60px auto 0;
                width: 30%;
            }
            svg {
                display: block;
                width: 30%;
                margin: -60px auto 0;
                .cls-1 {
                    fill: none;
                    stroke: #000;
                    stroke-miterlimit: 10;
                    stroke-width: 50px;
                }
            }
            .to-the-info {
                display: flex;
                justify-content: center;
                align-items: center;
                
                width: 70px;
                height: 70px;
                border-radius: 50px;
                cursor: pointer;
                margin: 0 auto;
                transition: 0.8s;
            }
            .to-the-info:hover {
                box-shadow: 0 0 7px #fff,
                    0 0 10px rgb(237, 245, 253),
                    0 0 21px rgb(208, 230, 255),
                    0 0 30px rgb(175, 214, 255),
                    0 0 50px rgb(142, 197, 255),
                    0 0 70px rgb(126, 188, 255),
                    0 0 90px rgb(120, 185, 255),
                    0 0 120px rgb(94, 171, 254);
            }
            .to-the-info::before, .to-the-info::after {
                content: '';
                display: block;
                width: 20px;
                height: 2px;
                background-color: black;
                
            }
            .to-the-info::before {
                transform: rotate(45deg);
                margin-right: -3px;
            }
            .to-the-info::after {
                transform: rotate(-45deg);
                margin-left: -3px;
            }
            
        }
    }

    @media (max-width: 1599px) {
        .slogan-wrapper {
        padding-top: 150px;
        box-sizing: border-box;
        height: 100vh;
            .slogan-block {
                h1 {
                    text-align: center;
                    font-family: 'Kanit', sans-serif;
                    font-size: 68px; 
                    font-weight: 700;
                    letter-spacing: 2px;
                    span {
                        letter-spacing: 1px;
                        color: rgb(94, 171, 254);
                    }
                }
                img {
                    display: block;
                    margin: -30px auto 0;
                    width: 30%;
                }
                svg {
                    display: block;
                    width: 30%;
                    margin: -60px auto 3vh;
                    .cls-1 {
                        fill: none;
                        stroke: #000;
                        stroke-miterlimit: 10;
                        stroke-width: 50px;
                    }
                }
                .to-the-info {
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    
                    width: 70px;
                    height: 70px;
                    border-radius: 50px;
                    cursor: pointer;
                    margin: 0 auto;
                    transition: 0.8s;
                }
                .to-the-info:hover {
                    box-shadow: 0 0 7px #fff,
                        0 0 10px rgb(237, 245, 253),
                        0 0 21px rgb(208, 230, 255),
                        0 0 30px rgb(175, 214, 255),
                        0 0 50px rgb(142, 197, 255),
                        0 0 70px rgb(126, 188, 255),
                        0 0 90px rgb(120, 185, 255),
                        0 0 120px rgb(94, 171, 254);
                }
                .to-the-info::before, .to-the-info::after {
                    content: '';
                    display: block;
                    width: 20px;
                    height: 2px;
                    background-color: black;
                    
                }
                .to-the-info::before {
                    transform: rotate(45deg);
                    margin-right: -3px;
                }
                .to-the-info::after {
                    transform: rotate(-45deg);
                    margin-left: -3px;
                }
                
            }
        }
    }
    @media (max-width: 1200px) {
        .slogan-wrapper {
        padding-top: 150px;
        box-sizing: border-box;
        height: 100vh;
            .slogan-block {
                h1 {
                    text-align: center;
                    font-family: 'Kanit', sans-serif;
                    font-size: 68px; 
                    font-weight: 700;
                    letter-spacing: 2px;
                    span {
                        letter-spacing: 1px;
                        color: rgb(94, 171, 254);
                    }
                }
                img {
                    display: block;
                    margin: -30px auto 0;
                    width: 30%;
                }
                svg {
                    display: block;
                    width: 30%;
                    margin: -60px auto 10vh;
                    .cls-1 {
                        fill: none;
                        stroke: #000;
                        stroke-miterlimit: 10;
                        stroke-width: 50px;
                    }
                }
                .to-the-info {
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    
                    width: 70px;
                    height: 70px;
                    border-radius: 50px;
                    cursor: pointer;
                    margin: 0 auto;
                    transition: 0.8s;
                }
                .to-the-info:hover {
                    box-shadow: 0 0 7px #fff,
                        0 0 10px rgb(237, 245, 253),
                        0 0 21px rgb(208, 230, 255),
                        0 0 30px rgb(175, 214, 255),
                        0 0 50px rgb(142, 197, 255),
                        0 0 70px rgb(126, 188, 255),
                        0 0 90px rgb(120, 185, 255),
                        0 0 120px rgb(94, 171, 254);
                }
                .to-the-info::before, .to-the-info::after {
                    content: '';
                    display: block;
                    width: 20px;
                    height: 2px;
                    background-color: black;
                    
                }
                .to-the-info::before {
                    transform: rotate(45deg);
                    margin-right: -3px;
                }
                .to-the-info::after {
                    transform: rotate(-45deg);
                    margin-left: -3px;
                }
                
            }
        }    
    }
    @media (max-width: 1024px) {
        .slogan-wrapper {
        padding-top: 150px;
        box-sizing: border-box;
        height: 100vh;
            .slogan-block {
                h1 {
                    text-align: center;
                    font-family: 'Kanit', sans-serif;
                    font-size: 55px; 
                    font-weight: 700;
                    letter-spacing: 2px;
                    span {
                        letter-spacing: 1px;
                        color: rgb(94, 171, 254);
                    }
                }
                img {
                    display: block;
                    margin: 0px auto 0;
                    width: 30%;
                }
                svg {
                    display: block;
                    width: 30%;
                    margin: 0 auto 14vh ;
                    .cls-1 {
                        fill: none;
                        stroke: #000;
                        stroke-miterlimit: 10;
                        stroke-width: 50px;
                    }
                }
                .to-the-info {
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    
                    width: 70px;
                    height: 70px;
                    border-radius: 50px;
                    cursor: pointer;
                    margin: 0 auto;
                    transition: 0.8s;
                }
                .to-the-info:hover {
                    box-shadow: 0 0 7px #fff,
                        0 0 10px rgb(237, 245, 253),
                        0 0 21px rgb(208, 230, 255),
                        0 0 30px rgb(175, 214, 255),
                        0 0 50px rgb(142, 197, 255),
                        0 0 70px rgb(126, 188, 255),
                        0 0 90px rgb(120, 185, 255),
                        0 0 120px rgb(94, 171, 254);
                }
                .to-the-info::before, .to-the-info::after {
                    content: '';
                    display: block;
                    width: 20px;
                    height: 2px;
                    background-color: black;
                    
                }
                .to-the-info::before {
                    transform: rotate(45deg);
                    margin-right: -3px;
                }
                .to-the-info::after {
                    transform: rotate(-45deg);
                    margin-left: -3px;
                }
                
            }
        }
    }
    @media (max-width: 767px) {
        .slogan-wrapper {
        padding-top: 150px;
        box-sizing: border-box;
        height: 100vh;
            .slogan-block {
                h1 {
                    text-align: center;
                    font-family: 'Kanit', sans-serif;
                    font-size: 40px; 
                    font-weight: 700;
                    letter-spacing: 2px;
                    span {
                        letter-spacing: 1px;
                        color: rgb(94, 171, 254);
                    }
                }
                img {
                    display: block;
                    margin: 0px auto 0;
                    width: 30%;
                }
                svg {
                    display: block;
                    width: 80%;
                    margin: 0 auto 2vh ;
                    .cls-1 {
                        fill: none;
                        stroke: #000;
                        stroke-miterlimit: 10;
                        stroke-width: 50px;
                    }
                }
                .to-the-info {
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    
                    width: 70px;
                    height: 70px;
                    border-radius: 50px;
                    cursor: pointer;
                    margin: 0 auto;
                    transition: 0.8s;
                }
                .to-the-info:hover {
                    box-shadow: 0 0 7px #fff,
                        0 0 10px rgb(237, 245, 253),
                        0 0 21px rgb(208, 230, 255),
                        0 0 30px rgb(175, 214, 255),
                        0 0 50px rgb(142, 197, 255),
                        0 0 70px rgb(126, 188, 255),
                        0 0 90px rgb(120, 185, 255),
                        0 0 120px rgb(94, 171, 254);
                }
                .to-the-info::before, .to-the-info::after {
                    content: '';
                    display: block;
                    width: 20px;
                    height: 2px;
                    background-color: black;
                    
                }
                .to-the-info::before {
                    transform: rotate(45deg);
                    margin-right: -3px;
                }
                .to-the-info::after {
                    transform: rotate(-45deg);
                    margin-left: -3px;
                }
                
            }
        }
    }

    @media (max-width: 400px) {
        .slogan-wrapper {
        padding-top: 150px;
        box-sizing: border-box;
        height: 100vh;
            .slogan-block {
                h1 {
                    text-align: center;
                    font-family: 'Kanit', sans-serif;
                    font-size: 25px; 
                    font-weight: 700;
                    letter-spacing: 2px;
                    span {
                        letter-spacing: 1px;
                        color: rgb(94, 171, 254);
                    }
                }
                img {
                    display: block;
                    margin: 0px auto 0;
                    width: 30%;
                }
                svg {
                    display: block;
                    width: 70%;
                    margin: 0 auto 9vh;
                    .cls-1 {
                        fill: none;
                        stroke: #000;
                        stroke-miterlimit: 10;
                        stroke-width: 50px;
                    }
                }
                .to-the-info {
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    
                    width: 70px;
                    height: 70px;
                    border-radius: 50px;
                    cursor: pointer;
                    margin: 0 auto;
                    transition: 0.8s;
                }
                .to-the-info:hover {
                    box-shadow: 0 0 7px #fff,
                        0 0 10px rgb(237, 245, 253),
                        0 0 21px rgb(208, 230, 255),
                        0 0 30px rgb(175, 214, 255),
                        0 0 50px rgb(142, 197, 255),
                        0 0 70px rgb(126, 188, 255),
                        0 0 90px rgb(120, 185, 255),
                        0 0 120px rgb(94, 171, 254);
                }
                .to-the-info::before, .to-the-info::after {
                    content: '';
                    display: block;
                    width: 20px;
                    height: 2px;
                    background-color: black;
                    
                }
                .to-the-info::before {
                    transform: rotate(45deg);
                    margin-right: -3px;
                }
                .to-the-info::after {
                    transform: rotate(-45deg);
                    margin-left: -3px;
                }
                
            }
        }
        @media (max-height: 900px) {
            .slogan-wrapper {
        padding-top: 150px;
        box-sizing: border-box;
        height: 100vh;
            .slogan-block {
                h1 {
                    text-align: center;
                    font-family: 'Kanit', sans-serif;
                    font-size: 25px; 
                    font-weight: 700;
                    letter-spacing: 2px;
                    span {
                        letter-spacing: 1px;
                        color: rgb(94, 171, 254);
                    }
                }
                img {
                    display: block;
                    margin: 0px auto 0;
                    width: 30%;
                }
                svg {
                    display: block;
                    width: 70%;
                    margin: 0 auto 20vh;
                    .cls-1 {
                        fill: none;
                        stroke: #000;
                        stroke-miterlimit: 10;
                        stroke-width: 50px;
                    }
                }
                .to-the-info {
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    
                    width: 70px;
                    height: 70px;
                    border-radius: 50px;
                    cursor: pointer;
                    margin: 0 auto;
                    transition: 0.8s;
                }
                .to-the-info:hover {
                    box-shadow: 0 0 7px #fff,
                        0 0 10px rgb(237, 245, 253),
                        0 0 21px rgb(208, 230, 255),
                        0 0 30px rgb(175, 214, 255),
                        0 0 50px rgb(142, 197, 255),
                        0 0 70px rgb(126, 188, 255),
                        0 0 90px rgb(120, 185, 255),
                        0 0 120px rgb(94, 171, 254);
                }
                .to-the-info::before, .to-the-info::after {
                    content: '';
                    display: block;
                    width: 20px;
                    height: 2px;
                    background-color: black;
                    
                }
                .to-the-info::before {
                    transform: rotate(45deg);
                    margin-right: -3px;
                }
                .to-the-info::after {
                    transform: rotate(-45deg);
                    margin-left: -3px;
                }
                
            }
        }
        }
    }
</style>
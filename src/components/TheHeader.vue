<template>
    <div class="header-wrapper">

        <div class="logo-block">
            <svg id="_Слой_1" data-name="Слой 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1024 1024">
                <circle class="cls-1" cx="511.57" cy="514.25" r="237"/>
                <g>
                    <rect x="521.63" y="232.7" width="50" height="627.91" rx="10.21" ry="10.21" transform="translate(546.65 -226.41) rotate(45)"/>
                    <rect x="452.49" y="164.65" width="50" height="627.91" rx="10.21" ry="10.21" transform="translate(478.28 -197.46) rotate(45)"/>
                </g>
            </svg>
            <h1>OpenCoin</h1>
        </div>

        <div class="cost-and-tg-block">
            <div class="link-tg-block">
                <a href="https://t.me/OpenCoinCommunity" target="_blank">@OpenCoinCommunity</a>
            </div>
            <div class="cost-block">
                <p>1 $OPEN = {{ cost }} TON</p>
                <img src="../assets/arrow-up.png">
            </div>
        </div>
    </div>
</template>

<script>


    export default {
        name: 'TheHeader',
        data() {
            return {
                cost: ''
            }
        },
        mounted() {
            setInterval(() => {
                fetch('https://api.dyor.io/api/v3/analytics?currency=jUSDT&lite=1&page=1&pairs=1151&period=all')
                .then(response => response.json())
                .then(data => {
                    this.cost = Number(data["lastPrices"][1151]["price"]["price"])
                    this.cost = this.cost.toFixed(4)
                })
            }, 500);
        }
    }
</script>

<style scoped lang="scss">
    .header-wrapper {
        background-color: white;
        position: fixed;
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 100%;
        height: 100px;

        padding: 22px calc(100%/10) 0;
        box-sizing: border-box;
        .logo-block {
            display: flex;
            align-items: center;
            svg {
                width: 50px;
                height: 50px;

                .cls-1 {
                    fill: none;
                    stroke: #000;
                    stroke-miterlimit: 10;
                    stroke-width: 50px;
                }
            }
            h1 {
                font-family: 'Kanit', sans-serif;
                font-weight: 700;
                font-size: 22px;
                -webkit-touch-callout: none; /* iOS Safari */
                -webkit-user-select: none; /* Safari */
                -khtml-user-select: none; /* Konqueror HTML */
                -moz-user-select: none; /* Old versions of Firefox */
                -ms-user-select: none; /* Internet Explorer/Edge */
                user-select: none; 
                cursor: default;
            }
        }
        .cost-and-tg-block {
            display: flex;
            flex-direction: row-reverse;
            .cost-block {
                display: flex;
                p {
                    font-family: 'Kanit', sans-serif;
                    font-weight: 300;
                    font-size: 18px;
                }
                img {
                    margin-left: 4px;
                    width: 20px;
                }
            }
            .link-tg-block {
                margin: 0 50px 0 60px;
                box-sizing: border-box;
                a {
                    font-family: 'Kanit', sans-serif;
                    font-weight: 300;
                    font-size: 18px;
                    position: relative;
                    text-decoration: none;
                    color: black;
                }

                a:after {
                    content: '';
                    position: absolute;
                    right: 0;
                    bottom: -10px;
                    height: 5px;
                    width: 0;
                    background-color: rgb(28, 116, 204);
                    transition: width 0.3s ease-out;
                }

                a:hover:after {
                    right: auto;
                    left: 0;
                    width: 100%;
                }

                a:hover {
                    text-decoration: none;
                }
            }
        }
    }

    @media (max-width: 1599px) {
        // .header-wrapper {
        //     background-color: white;
        //     position: fixed;
        //     display: flex;
        //     align-items: center;
        //     justify-content: space-around;
        //     width: 100%;
        //     height: 100px;

        //     padding: 22px 15px 0;
        //     box-sizing: border-box;
        //     .logo-block {
        //         display: flex;
        //         align-items: center;
        //         svg {
        //             width: 50px;
        //             height: 50px;

        //             .cls-1 {
        //                 fill: none;
        //                 stroke: #000;
        //                 stroke-miterlimit: 10;
        //                 stroke-width: 50px;
        //             }
        //         }
        //         h1 {
        //             font-family: 'Kanit', sans-serif;
        //             font-weight: 700;
        //             font-size: calc(100%/1);
        //         }
        //     }
        //     .cost-and-tg-block {
        //         display: block;
        //         .cost-block {
        //             display: flex;
        //             p {
        //                 font-family: 'Kanit', sans-serif;
        //                 font-weight: 300;
        //                 font-size: calc(100%/1.2);

        //             }
        //             img {
        //                 margin-left: 4px;
        //                 width: 20px;
        //             }
        //         }
        //         .link-tg-block {
        //             margin: 0;
        //             margin-top: 10px;
        //             margin-bottom: 15px;
        //             box-sizing: border-box;
        //             a {
        //                 font-family: 'Kanit', sans-serif;
        //                 font-weight: 300;
        //                 font-size: calc(100%/1);
        //             }
        //         }
        //     }
        // }
    }

    @media (max-width: 1024px) {
        .header-wrapper {
            background-color: white;
            position: fixed;
            display: flex;
            align-items: center;
            justify-content: space-around;
            width: 100%;
            height: 100px;

            padding: 22px 15px 0;
            box-sizing: border-box;
            .logo-block {
                display: flex;
                align-items: center;
                svg {
                    width: 50px;
                    height: 50px;

                    .cls-1 {
                        fill: none;
                        stroke: #000;
                        stroke-miterlimit: 10;
                        stroke-width: 50px;
                    }
                }
                h1 {
                    font-family: 'Kanit', sans-serif;
                    font-weight: 700;
                    font-size: calc(100%/1);
                }
            }
            .cost-and-tg-block {
                display: block;
                .cost-block {
                    display: flex;
                    p {
                        font-family: 'Kanit', sans-serif;
                        font-weight: 300;
                        font-size: calc(100%/1.1);

                    }
                    img {
                        margin-left: 4px;
                        width: 20px;
                    }
                }
                .link-tg-block {
                    margin: 0;
                    margin-top: 10px;
                    margin-bottom: 15px;
                    box-sizing: border-box;
                    a {
                        font-family: 'Kanit', sans-serif;
                        font-weight: 300;
                        font-size: calc(100%/1.1);
                    }
                }
            }
        }
    }

    @media (max-width: 767px) {
        .header-wrapper {
            background-color: white;
            position: fixed;
            display: flex;
            align-items: center;
            justify-content: space-around;
            width: 100%;
            height: 100px;

            padding: 22px 15px 0;
            box-sizing: border-box;
            .logo-block {
                display: flex;
                align-items: center;
                svg {
                    width: 50px;
                    height: 50px;

                    .cls-1 {
                        fill: none;
                        stroke: #000;
                        stroke-miterlimit: 10;
                        stroke-width: 50px;
                    }
                }
                h1 {
                    font-family: 'Kanit', sans-serif;
                    font-weight: 700;
                    font-size: calc(100%/1.2);
                }
            }
            .cost-and-tg-block {
                display: block;
                .cost-block {
                    display: flex;
                    p {
                        font-family: 'Kanit', sans-serif;
                        font-weight: 300;
                        font-size: calc(100%/1.5);

                    }
                    img {
                        margin-left: 4px;
                        width: 20px;
                    }
                }
                .link-tg-block {
                    margin: 0;
                    margin-top: 10px;
                    margin-bottom: 15px;
                    box-sizing: border-box;
                    a {
                        font-family: 'Kanit', sans-serif;
                        font-weight: 300;
                        font-size: calc(100%/1.5);
                    }
                }
            }
        }
    }

    @media (max-width: 400px) {
        .cost-block {
                    display: flex;
                    p {
                        font-family: 'Kanit', sans-serif;
                        font-weight: 300;
                        font-size: calc(100%/4);

                    }
                    img {
                        margin-left: 4px;
                        width: 20px;
                    }
                }
        .link-tg-block {
                    margin: 0;
                    margin-top: 10px;
                    margin-bottom: 15px;
                    box-sizing: border-box;
                    a {
                        font-family: 'Kanit', sans-serif;
                        font-weight: 300;
                        font-size: calc(100%/2.9);
                    }
                }
    }
</style>
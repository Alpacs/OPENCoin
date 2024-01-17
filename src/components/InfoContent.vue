<template>
    <div id="info" class="wrapper-info-block">
        <div class="info-block">
            <p class="preview-info-text">Info</p>
            <div class="info">

                <div class="contract-block">
                    <h1>Contract</h1>
                    <div class="contract-copy-block">
                        <span><p>EQDf84FT8tdHZeI2-LXdb8gPMRqHRSABrmi8jI7MzvVpGJKZ</p></span>
                        <button :style="`cursor: ${buttonCursor};`" @click="copiedContract()">{{ copiedCheck }}</button>
                    </div>
                </div>

                <div class="max-supply-block">
                    <h1>Max. supply</h1>
                    <span><p>10.000.000 $OPEN</p></span>
                </div>

                <div class="about-us-block">
                    <h1>About us</h1>
                    <span><p>Open coin for open community</p></span>
                </div>

            </div>
        </div>
    </div>
</template>

<script>

export default {
    name: 'InfoContent',
    data() {
        return {
            copiedCheck: 'Copy',
            buttonCursor: 'pointer'
        }
    },
    methods: {
        copiedContract() {
            navigator.clipboard.writeText('EQDf84FT8tdHZeI2-LXdb8gPMRqHRSABrmi8jI7MzvVpGJKZ');
            this.copiedCheck = 'Done!'
            this.buttonCursor = 'default'
        }
    }
}

</script>

<style scoped lang="scss">

    .wrapper-info-block {
        display: flex;
        align-items: center;
        justify-content: center;
        width: 100%;
        height: 85vh;
        box-sizing: border-box;
        .info-block {
            display: block;
            margin: 0 auto;
            width: 45%;
            .preview-info-text {
                margin-left: 20px;
                margin-bottom: 10px;
                font-family: 'Kanit', sans-serif;
                font-weight: 600;
                font-size: calc(100vw/38.4);
            }
            .info {
                display: block;
                width: 100%;
                background-color: black;
                padding: 30px;
                border-radius: 10px;
                .contract-block {
                    margin-bottom: 30px;
                    h1 {
                        font-family: 'Kanit', sans-serif;
                        font-weight: 600;
                        font-size: calc(100vw/48);
                        color: white;
                        margin-bottom: calc(100vw/160);
                        margin-left: 10px;
                    }
                    .contract-copy-block {
                        display: flex;
                        align-content: stretch;
                        justify-content: space-between;
                        
                        span {
                            width: 82%;
                            background-color: rgb(184, 210, 235);
                            text-align: center;
                            border-radius: 10px;
                            p {
                                padding: 10px;
                                font-family: 'Kanit', sans-serif;
                                font-weight: 300;
                                font-size: calc(100vw/75);
                                -webkit-line-clamp: 1;
                                overflow: hidden;
                                text-overflow: ellipsis;
                            }
                        }
                        button {
                            width: 15%;
                            border: 0;
                            background-color: white;
                            font-family: 'Kanit', sans-serif;
                            font-weight: 300;
                            font-size: calc(100vw/75);
                            border-radius: 10px;
                        }
                    }
                }

                .max-supply-block {
                    margin-bottom: 30px;
                    h1 {
                        font-family: 'Kanit', sans-serif;
                        font-weight: 600;
                        font-size: calc(100vw/48);
                        color: white;
                        margin-bottom: calc(100vw/160);
                        margin-left: 10px;
                    }
                    span {
                        display: inline-block;
                        background-color: rgb(184, 210, 235);
                        border-radius: 10px;
                        p {
                            padding: 12px;
                            font-family: 'Kanit', sans-serif;
                            font-weight: 300;
                            font-size: calc(100vw/75);
                        }
                    }
                }

                .about-us-block {
                    h1 {
                        font-family: 'Kanit', sans-serif;
                        font-weight: 600;
                        font-size: calc(100vw/48);
                        color: white;
                        margin-bottom: calc(100vw/160);
                        margin-left: 10px;
                    }
                    span {
                        display: inline-block;
                        background-color: rgb(184, 210, 235);
                        border-radius: 10px;
                        p {
                            padding: 10px;
                            font-family: 'Kanit', sans-serif;
                            font-weight: 300;
                            font-size: calc(100vw/75);
                        }
                    }
                }
            }
        }
    }
    
    @media (max-width: 1599px) {
        .wrapper-info-block {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 100%;
            height: 85vh;
            box-sizing: border-box;
            .info-block {
                display: block;
                margin: 0 auto;
                width: 45%;
                .preview-info-text {
                    margin-left: 20px;
                    font-family: 'Kanit', sans-serif;
                    font-weight: 600;
                    font-size: calc(100vw/32);
                }
                .info {
                    display: block;
                    width: 100%;
                    border-radius: 10px;
                    background-color: black;
                    padding: 30px;
                    .contract-block {
                        margin-bottom: 30px;
                        h1 {
                            font-family: 'Kanit', sans-serif;
                            font-weight: 600;
                            font-size: calc(100vw/53.3);
                            color: white;
                            margin-bottom: 5px;
                            margin-left: 10px;
                        }
                        .contract-copy-block {
                            display: flex;
                            align-content: stretch;
                            justify-content: space-between;
                            
                            span {
                                width: 85%;
                                background-color: rgb(184, 210, 235);
                                text-align: center;
                                border-radius: 10px;
                                p {
                                    padding: 10px;
                                    font-family: 'Kanit', sans-serif;
                                    font-weight: 300;
                                    font-size: calc(100vw/72);
                                }
                            }
                            button {
                                width: 12%;
                                border: 0;
                                border-radius: 10px;
                                background-color: white;
                                font-family: 'Kanit', sans-serif;
                                font-weight: 300;
                                font-size: calc(100vw/72);
                            }
                        }
                    }

                    .max-supply-block {
                        margin-bottom: 30px;
                        h1 {
                            font-family: 'Kanit', sans-serif;
                            font-weight: 600;
                            font-size: calc(100vw/53.3);
                            font-size: 30px;
                            color: white;
                            margin-bottom: 5px;
                            margin-left: 10px;
                        }
                        span {
                            display: inline-block;
                            background-color: rgb(184, 210, 235);
                            border-radius: 10px;
                            p {
                                padding: 10px;
                                font-family: 'Kanit', sans-serif;
                                font-weight: 300;
                                font-size: calc(100vw/72);
                            }
                        }
                    }

                    .about-us-block {
                        h1 {
                            font-family: 'Kanit', sans-serif;
                            font-weight: 600;
                            font-size: calc(100vw/53.3);
                            font-size: 30px;
                            color: white;
                            margin-bottom: 5px;
                            margin-left: 10px;
                        }
                        span {
                            display: inline-block;
                            background-color: rgb(184, 210, 235);
                            border-radius: 10px;
                            p {
                                padding: 10px;
                                font-family: 'Kanit', sans-serif;
                                font-weight: 300;
                                font-size: calc(100vw/72);
                            }
                        }
                    }
                }
            }
        }
    }
    @media (max-width: 1024px) {
        .wrapper-info-block {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 100%;
            height: 85vh;
            box-sizing: border-box;
            margin-bottom: 200px;
            .info-block {
                display: block;
                margin: 0 auto;
                width: 60%;
                .preview-info-text {
                    margin-left: 20px;
                    margin-bottom: 15px;
                    font-family: 'Kanit', sans-serif;
                    font-weight: 600;
                    font-size: calc(100vw/19.2);

                }
                .info {
                    display: block;
                    width: 100%;
                    background-color: black;
                    padding: 30px;
                    border-radius: 10px;
                    .contract-block {
                        margin-bottom: 50px;
                        h1 {
                            font-family: 'Kanit', sans-serif;
                            font-weight: 600;
                            font-size: calc(100vw/40);
                            color: white;
                            margin-bottom: 18px;
                            margin-left: 10px;
                        }
                        .contract-copy-block {
                            display: flex;
                            align-content: stretch;
                            justify-content: space-between;
                            
                            span {
                                display: flex;
                                justify-content: center;
                                align-items: center;
                                width: 77%;
                                background-color: rgb(184, 210, 235);
                                text-align: center;
                                border-radius: 10px;
                                p {
                                    padding: 0;
                                    font-family: 'Kanit', sans-serif;
                                    font-weight: 300;
                                    font-size: calc(100vw/60);
                                }
                            }
                            button {
                                width: 18%;
                                border: 0;
                                background-color: white;
                                font-family: 'Kanit', sans-serif;
                                font-weight: 300;
                                border-radius: 10px;
                                text-align: center;
                                font-size: calc(100vw/60);
                            }
                        }
                    }

                    .max-supply-block {
                        margin-bottom: 50px;
                        h1 {
                            font-family: 'Kanit', sans-serif;
                            font-weight: 600;
                            font-size: calc(100vw/40);
                            color: white;
                            margin-bottom: 18px;
                            margin-left: 10px;
                        }
                        span {
                            display: inline-block;
                            background-color: rgb(184, 210, 235);
                            border-radius: 10px;
                            p {
                                padding: 12px;
                                font-family: 'Kanit', sans-serif;
                                font-weight: 300;
                                font-size: calc(100vw/60);
                            }
                        }
                    }

                    .about-us-block {
                        
                        h1 {
                            font-family: 'Kanit', sans-serif;
                            font-weight: 600;
                            font-size: calc(100vw/40);
                            color: white;
                            margin-bottom: 18px;
                            margin-left: 10px;
                        }
                        span {
                            display: inline-block;
                            background-color: rgb(184, 210, 235);
                            border-radius: 10px;
                            p {
                                padding: 10px;
                                font-family: 'Kanit', sans-serif;
                                font-weight: 300;
                                font-size: calc(100vw/60);
                            }
                        }
                    }
                }
            }
        }
    }
    @media (max-width: 767px) {
        .wrapper-info-block {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 100%;
            height: 85vh;
            box-sizing: border-box;
            .info-block {
                display: block;
                margin: 0 auto;
                width: 80%;
                .preview-info-text {
                    margin-left: 20px;
                    margin-bottom: 15px;
                    font-family: 'Kanit', sans-serif;
                    font-weight: 600;
                    font-size: calc(100vw/10);
                }
                .info {
                    display: block;
                    width: 100%;
                    background-color: black;
                    padding: 30px;
                    box-sizing: border-box;
                    border-radius: 10px;
                    .contract-block {
                        margin-bottom: 20px;
                        h1 {
                            font-family: 'Kanit', sans-serif;
                            font-weight: 600;
                            font-size: calc(100vw/20);
                            color: white;
                            margin-bottom: 12px;
                            margin-left: 10px;
                        }
                        .contract-copy-block {
                            display: flex;
                            align-content: stretch;
                            justify-content: flex-start;
                            span {
                                display: flex;
                                justify-content: center;
                                align-items: center;
                                background-color: rgb(184, 210, 235);
                                text-align: center;
                                border-radius: 10px;
                                p {
                                    padding: 7px;
                                    font-family: 'Kanit', sans-serif;
                                    font-weight: 300;
                                    font-size: calc(100vw/35);
                                    white-space: nowrap;
                                    text-overflow: ellipsis;
                                }
                            }
                            button {
                                width: 14%;
                                margin-left: 10px;
                                border: 0;
                                background-color: white;
                                font-family: 'Kanit', sans-serif;
                                font-weight: 300;
                                border-radius: 10px;
                                text-align: center;
                                font-size: calc(100vw/35);
                            }
                        }
                    }

                    .max-supply-block {
                        margin-bottom: 20px;
                        h1 {
                            font-family: 'Kanit', sans-serif;
                            font-weight: 600;
                            font-size: calc(100vw/20);
                            color: white;
                            margin-bottom: 12px;
                            margin-left: 10px;
                        }
                        span {
                            display: inline-block;
                            background-color: rgb(184, 210, 235);
                            border-radius: 10px;
                            p {
                                padding: 7px;
                                font-family: 'Kanit', sans-serif;
                                font-weight: 300;
                                font-size: calc(100vw/35);
                            }
                        }
                    }

                    .about-us-block {
                        
                        h1 {
                            font-family: 'Kanit', sans-serif;
                            font-weight: 600;
                            font-size: calc(100vw/20);
                            color: white;
                            margin-bottom: 12px;
                            margin-left: 10px;
                        }
                        span {
                            display: inline-block;
                            background-color: rgb(184, 210, 235);
                            border-radius: 10px;
                            p {
                                padding: 7px;
                                font-family: 'Kanit', sans-serif;
                                font-weight: 300;
                                font-size: calc(100vw/35);
                            }
                        }
                    }
                }
            }
        }
    }
    // @media (max-width: 500px) {
    //     .wrapper-info-block {
    //         display: block;
    //         width: 100%;
    //         height: 85vh;
    //         box-sizing: border-box;
    //         padding-top: 80px;
    //         .info-block {
    //             display: block;
    //             margin: 0 auto;
    //             width: 60%;
    //             .preview-info-text {
    //                 margin-left: 20px;
    //                 margin-bottom: 15px;
    //                 font-family: 'Kanit', sans-serif;
    //                 font-weight: 600;
    //                 font-size: calc(100vw/25);
    //             }
    //             .info {
    //                 display: block;
    //                 width: 100%;
    //                 background-color: black;
    //                 padding: 30px;
    //                 box-sizing: border-box;
    //                 border-radius: 10px;
    //                 .contract-block {
    //                     margin-bottom: 20px;
    //                     h1 {
    //                         font-family: 'Kanit', sans-serif;
    //                         font-weight: 600;
    //                         font-size: calc(100vw/45);
    //                         color: white;
    //                         margin-bottom: 10px;
    //                         margin-left: 10px;
    //                     }
    //                     .contract-copy-block {
    //                         display: flex;
    //                         align-content: stretch;
    //                         justify-content: flex-start;
    //                         span {
    //                             display: flex;
    //                             justify-content: center;
    //                             align-items: center;
    //                             width: calc(100%/1.2);
    //                             background-color: rgb(184, 210, 235);
    //                             text-align: center;
    //                             border-radius: 10px;
    //                             p {
    //                                 padding: 8px;
    //                                 font-family: 'Kanit', sans-serif;
    //                                 font-weight: 300;
    //                                 font-size: calc(100vw/85);
    //                             }
    //                         }
    //                         button {
    //                             margin-left: 10px;
    //                             border: 0;
    //                             background-color: white;
    //                             font-family: 'Kanit', sans-serif;
    //                             font-weight: 300;
    //                             border-radius: 10px;
    //                             text-align: center;
    //                             font-size: calc(100vw/70);
    //                         }
    //                     }
    //                 }

    //                 .max-supply-block {
    //                     margin-bottom: 20px;
    //                     h1 {
    //                         font-family: 'Kanit', sans-serif;
    //                         font-weight: 600;
    //                         font-size: calc(100vw/45);
    //                         color: white;
    //                         margin-bottom: 10px;
    //                         margin-left: 10px;
    //                     }
    //                     span {
    //                         display: inline-block;
    //                         background-color: rgb(184, 210, 235);
    //                         border-radius: 10px;
    //                         p {
    //                             padding: 8px;
    //                             font-family: 'Kanit', sans-serif;
    //                             font-weight: 300;
    //                             font-size: calc(100vw/70);
    //                         }
    //                     }
    //                 }

    //                 .about-us-block {
                        
    //                     h1 {
    //                         font-family: 'Kanit', sans-serif;
    //                         font-weight: 600;
    //                         font-size: calc(100vw/45);
    //                         color: white;
    //                         margin-bottom: 10px;
    //                         margin-left: 10px;
    //                     }
    //                     span {
    //                         display: inline-block;
    //                         background-color: rgb(184, 210, 235);
    //                         border-radius: 10px;
    //                         p {
    //                             padding: 8px;
    //                             font-family: 'Kanit', sans-serif;
    //                             font-weight: 300;
    //                             font-size: calc(100vw/70);
    //                         }
    //                     }
    //                 }
    //             }
    //         }
    //     }
    // }
    @media (max-width: 400px) {
        .wrapper-info-block {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 100%;
            height: 85vh;
            box-sizing: border-box;
            .info-block {
                display: block;
                margin: 0 auto;
                width: 90%;
                .preview-info-text {
                    margin-left: 20px;
                    margin-bottom: 15px;
                    font-family: 'Kanit', sans-serif;
                    font-weight: 600;
                    font-size: calc(100vw/8);
                }
                .info {
                    display: block;
                    width: 100%;
                    background-color: black;
                    padding: 30px;
                    box-sizing: border-box;
                    border-radius: 10px;
                    .contract-block {
                        margin-bottom: 20px;
                        h1 {
                            font-family: 'Kanit', sans-serif;
                            font-weight: 600;
                            font-size: calc(100vw/13);
                            color: white;
                            margin-bottom: 10px;
                            margin-left: 10px;
                        }
                        .contract-copy-block {
                            display: flex;
                            align-content: stretch;
                            justify-content: flex-start;
                            span {
                                display: flex;
                                justify-content: center;
                                align-items: center;
                                width: calc(100%/2);
                                background-color: rgb(184, 210, 235);
                                text-align: center;
                                border-radius: 10px;
                                p {
                                    padding: 8px;
                                    font-family: 'Kanit', sans-serif;
                                    font-weight: 300;
                                    font-size: calc(100vw/25);
                                    text-overflow: ellipsis;
                                    white-space: nowrap;
                                }
                            }
                            button {
                                width: calc(100%/4);
                                margin-left: 10px;
                                border: 0;
                                background-color: white;
                                font-family: 'Kanit', sans-serif;
                                font-weight: 300;
                                border-radius: 10px;
                                text-align: center;
                                font-size: calc(100vw/25);
                            }
                        }
                    }

                    .max-supply-block {
                        margin-bottom: 20px;
                        h1 {
                            font-family: 'Kanit', sans-serif;
                            font-weight: 600;
                            font-size: calc(100vw/13);
                            color: white;
                            margin-bottom: 10px;
                            margin-left: 10px;
                        }
                        span {
                            display: inline-block;
                            background-color: rgb(184, 210, 235);
                            border-radius: 10px;
                            p {
                                padding: 8px;
                                font-family: 'Kanit', sans-serif;
                                font-weight: 300;
                                font-size: calc(100vw/25);
                            }
                        }
                    }

                    .about-us-block {
                        
                        h1 {
                            font-family: 'Kanit', sans-serif;
                            font-weight: 600;
                            font-size: calc(100vw/13);
                            color: white;
                            margin-bottom: 10px;
                            margin-left: 10px;
                        }
                        span {
                            display: inline-block;
                            background-color: rgb(184, 210, 235);
                            border-radius: 10px;
                            p {
                                padding: 8px;
                                font-family: 'Kanit', sans-serif;
                                font-weight: 300;
                                font-size: calc(100vw/25);
                            }
                        }
                    }
                }
            }
        }
    }
</style>
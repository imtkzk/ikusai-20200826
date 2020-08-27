<template>
    <div class="contents">
        <ul class="contents-in">
            <li class="title-big title-big-current">
                機械学習の3大トピック
                <ul class="list-inner">
                    <li class="title-small title-small-current">教師あり学習</li>
                    <li class="title-small">教師なし学習</li>
                </ul>
            </li>
            <li class="title-big">
                機械学習の3大トピック
            </li>
            <li class="title-big">
                機械学習の3大トピック
            </li>
            <li class="title-big">
                機械学習の3大トピック
            </li>
        </ul>
        <div class="share">
            <ul class="share-in">
                <li class="share-title">学んだ内容を共有する</li>
                <li class="icon share-facebook"><a href="#"><img src="~/assets/img/learn/icon-facebook.png" alt="Facebook"></a></li>
                <li class="icon share-twitter"><a href="#"><img src="~/assets/img/learn/icon-twitter.png" alt="twitter"></a></li>
            </ul>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";

    .contents{
        position: sticky;
        top:vw-pc(100);
        height: 600px;
        padding:vw-pc(20);
        width: vw-pc(400);
        font-weight: 600;
        .contents-in{
            border: vw-pc(3) solid #16325e;
            padding:vw-pc(30);
            margin-bottom:vw-pc(30);
            li{
                line-height: vw-pc(50);
                color: #acb6c7;
            }
             .title-big{
                 font-size: vw-pc(18);
                 .title-small{
                    font-size: vw-pc(15);
                    padding-left: vw-pc(20);
                 }
            }
            .title-big-current{
                color: #16325e;
            }
            .title-small-current{
                color: #16325e;
                border-radius: 2em;
                background-color: #f7f8f9;
            }
        }
        .share{
            border-radius: 6em;
            background-color: #f7f8f9;
            .share-in{
                display: flex;
                justify-content: space-between;
                align-items: center; 
                height: vw-pc(60);
                padding: 0 vw-pc(30);
                max-width: 450px;
                .icon{
                    width: vw-pc(30);
                    img{
                        width: 100%;
                    }
                }
                .share-title{
                    vertical-align: middle;
                }
                .share-title::before{
                    content:"";
                    display: inline-block;
                    height: vw-pc(18);
                    width: vw-pc(18);
                    background-size: contain;
                    background-repeat: no-repeat;
                    background-image: url(~assets/img/learn/share-title.png);
                    margin-right: vw-pc(10);
                }
            }
        }
    }
    @media screen and (max-width: $breakpoint1-max) {
    .contents{
        position: static;
        top:0;
        height: auto;
        padding:vw-sp(20);
        width: 100%;
        .contents-in{
            border: vw-sp(3) solid #16325e;
            padding:vw-sp(30);
            margin-bottom:vw-sp(30);
            li{
                line-height: vw-sp(50);
            }
             .title-big{
                 font-size: vw-sp(18);
                 .title-small{
                    font-size: vw-sp(15);
                    padding-left: vw-sp(20);
                 }
            }
        }
        .share{
            .share-in{
                height: vw-sp(60);
                padding: 0 vw-sp(30);
                max-width: vw-sp(400);
                .icon{
                    width: vw-sp(30);
                }
                .share-title{
                    font-size: vw-sp(15);
                }
                .share-title::before{
                    height: vw-sp(18);
                    width: vw-sp(18);
                    margin-right: vw-sp(10);
                }
            }
        }
    }
    }

    @media screen and (min-width: $breakpoint2) {
    .contents{
        top:100px;
        width: 400px;
        padding:20px;
        .contents-in{
            border: 3px solid #16325e;
            padding:30px;
            margin-bottom:30px;
            li{
                line-height: 50px;
            }
             .title-big{
                 font-size: 18px;
                 font-size: 1.8rem;
                 .title-small{
                    font-size: 15px;
                    padding-left: 20px;
                 }
            }
        }
        .share{
            .share-in{
                height: 60px;
                padding: 0 30px;
                max-width: 400px;
                .icon{
                    width: 30px;
                }
                .share-title{
                    font-size: 15px;
                }
                .share-title::before{
                    height: 18px;
                    width: 18px;
                    margin-right: 10px;
                }
            }
        }
    }
}
</style>
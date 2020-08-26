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
                height: vw-pc(80);
                padding: 0 vw-pc(30);
                .icon{
                    width: vw-pc(30);
                    img{
                        width: 100%;
                    }
                }
                .share-title::before{
                    content:"";
                    position: relative;
                    top: vw-pc(3);
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
</style>
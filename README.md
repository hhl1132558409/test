<!DOCTYPE HTML>
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">

<head>
    <title>表白网页</title>
    <meta http-equiv="content-type" content="text/html; charset=UTF-8">


    <style type="text/css">
        @font-face {
            font-family: digit;
            src: url('digital-7_mono.ttf') format("truetype");
        }
    </style>
    <link href="style/default.css" type="text/css" rel="stylesheet">
    <script type="text/javascript" src="style/jquery.js"></script>
    <script type="text/javascript" src="style/garden.js"></script>
    <script type="text/javascript" src="style/functions.js"></script>
</head>

<body>
    <div id="mainDiv">
        <div id="content">
            <div id="code">
                <p><span class="comments">/**</span><br />
                    <span class="space" /><span class="comments">*宝贝我爱你</span><br />
                    <span class="space" /><span class="comments">*/</span><br />
                    <span class="comments">// （其实我在五一期间就已经开始做网页了，给你的一定是我认为最完美的杰作）</span><br />
                    <br />
                    <span class="comments">// 当5月20号的时针走到5.20那一刻，这个网页会伴随着钟声来到你心里</span><br />
                </p>
                <p></p><span class="comments">// 当做情人节的小礼物，也给你出乎意料的惊喜</span><br />
                </p>
                <p><span class="comments">// 我爱你，宝，这个世界上最幸福的人一定是跟我在一起之后的你</span><br />
                    <br />
                    <span class="comments">// 我想给你太多太多的惊喜，给你做手工，拼拼图，拼DIY；</span><br />
                </p>
                <p><span class="comments">// 给你叠千纸鹤，叠纸爱心，叠纸玫瑰；带你去看电影，听音乐会，逛娃娃展；</span><br />
                    <br />
                    <span class="comments">// 总之太多太多的惊喜想要同你一起，我相信这些都会在以后慢慢的实现；</span>
                </p>
                <p><span class="comments">// 我还想手写情书寄给你，转念一想，也许做个网页你会更开心</span></p>
                <p><span class="comments">// 不如就把情书写在网页里，就像惊喜总是在不轻易间悄然而至</span><br />
                    <br />
                    <span class="comments">// 我把对你的爱藏在字里行间，慢慢等你去发现</span><br />
                </p>

            </div>
            <div id="loveHeart">
                <canvas id="garden"></canvas>
                <div id="words">
                    <div id="messages">
                        <center>
                            宝贝我爱你
                        </center>
                        <div id="elapseClock" style="display:none;text-align: center;"></div>
                        <a href='index2.html' id="accept" style="padding-left: 120px;text-decoration: none;">&nbsp;&nbsp;&nbsp;亲爱的，请点击这里</a>
                    </div>
                    <div id="words">
                        <div id="loveu" style="margin-top: 10px;">
                            爱你，直到永永远远。<br />
                            <div class="signature">- </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="bg1">
            <div class="main">
                <footer style="line-height:20px">
                    <div id="copyright">
                        <a href='' target="_blank"></a>

                        </object>
                    </div>
            </div>
        </div>
    </div>

    <script type="text/javascript">
        var offsetX = $("#loveHeart").width() / 2;
        var offsetY = $("#loveHeart").height() / 2 - 55;

        // 指定时间
        var time = 'Mon April 5 2021 11:58:53 GMT+0800 (中国标准时间)';
        // var together = new Date();
        // console.log(together);
        // var tog = formatDate(together);
        
        timeElapse(time);
        setInterval(function () {
            timeElapse(time);
        }, 500)

       
        if (!document.createElement('canvas').getContext) {
            $("#elapseClock").show();
                // var together = new Date();
                // timeElapse(together);
                // setInterval(function () {
                //     timeElapse(together);
                // }, 500);
            var msg = document.createElement("div");
            msg.id = "errorMsg";
            msg.innerHTML = "Your browser doesn't support HTML5!<br/>Recommend use Chrome 14+/IE 9+/Firefox 7+/Safari 4+";
            document.body.appendChild(msg);
            $("#code").css("display", "none")
            $("#copyright").css("position", "absolute");
            $("#copyright").css("bottom", "10px");
            document.execCommand("stop");
        } else {
            setTimeout(function () {
                adjustWordsPosition();
                startHeartAnimation();
            }, 10000);
            $("#elapseClock").show();
                // var together = new Date();
                // timeElapse(together);
                // setInterval(function () {
                //     timeElapse(together);
                // }, 500);
            $("#accept").click(function () {
                $(this).hide();

            })
            adjustCodePosition();
            $("#code").typewriter();
        }
    </script>
</body>
<audio id="bgmMusic" src="http://qzone.haoduoge.com/music/C2C3F0LSXH4D771253124A26CF9C71C939B2A.mp3" preload="auto"
    type="audio/mp3" autoplay loop></audio>

</html>

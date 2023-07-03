# 《Web应用基础》课程结业报告

### 1.网页内容：围绕《罗小黑战记》这个动漫的基本情况和历史和人物角色，角色关系和精彩片段做了一系列的介绍

### 2.开发过程：
>一开始对于整个网络的布局，我并没有什么头绪，所以我在b站上搜索了一些别人做的静态网页。<br>
>参考了几个过后，我发现基本上都是需要一个好看的导航栏，还要有高清的图片作为展示，<br>
>导航栏有时候跳转时间太长的话，效果没有在单个长页面跳转的视觉效果好，所以我就采用了这些设计:
- Bootstrap的导航栏样式
- 把多个html之间的页面跳转换为了在一个长页面中跳转
- 多多挑选了一些好看的照片作为图标、插图，从而美化页面
------------------------
<h4>1.导航栏</h4>
我先写了一段使用Bootstrap框架的导航栏的HTML代码。它包括一个标志、一个小屏幕上可折叠的菜单按钮以及链接到网站不同部分的链接。导航栏的最后一项是一个音频播放器，在网站加载时自动播放一首歌曲。

```html
 <!--导航-->
    <nav class="navbar navbar-default">
        <div class="container">
            <div class="navbar-header">
                <button class="navbar-toggle" data-toggle="collapse" data-target=".navbar-collapse">
                    <span class="icon-bar"></span>
                    <span class="icon-bar"></span>
                    <span class="icon-bar"></span>
                </button>
                <a href="" class="navbar-brand"><img alt="罗小黑 Logo" width="200" height="70"
                        src="images/OIP (2).png"
                        style="margin-right:20px;"></a>
            </div>
            <!--导航-->
            <div class="navbar-collapse collapse">
                <ul class="nav navbar-nav">
                    <li><a href="#home">主页</a></li>
                    <li><a href="#history">历史</a></li>
                    <li><a href="#bootstrap">获奖</a></li>
                    <li><a href="#course">其他人物</a></li>
                    <li><a href="#contact">联系我们</a></li>
                </ul>
                <ul class="nav navbar-nav navbar-right">
                    <li ><audio src="song/艾索 - 嘿咻狂想曲.ogg" controls autoplay="autoplay" style="margin-top: 8px;"></audio></li>
                </ul>
            </div>
            <!--导航-->
        </div>
    </nav>
    <!--导航-->
```
"nav"标签定义了导航栏，“navbar”和“navbar-default”类用于对其进行样式设置。“container”类用于居中导航栏的内容。

“navbar-header”类包含了标志和可折叠菜单按钮。“navbar-brand”类用于网站标志，“img”标签指定了图像的来源和尺寸。

“navbar-collapse”类用于在小屏幕上折叠菜单，“data-toggle”和“data-target”属性用于指定应折叠的元素。“nav”标签包含了链接到网站不同部分的链接，“navbar-nav”类用于样式化链接。

“navbar-right”类用于将音频播放器对齐到导航栏的右侧。“audio”标签指定了音频文件的来源，“controls”和“autoplay”属性用于添加播放控件并在网站加载时自动播放音频文件。

在CSS文件中，我给这个导航栏添加了样式：

```css
.navbar {
    margin-bottom: 0;
    border-bottom: 1px solid #e6e6e6;
}

.navbar-default {
    background-color: #fff;
}

.navbar-default .navbar-brand {
    font-size: 30px;
    font-weight: bold;
    height: 70px;
    line-height: 35px;
    padding: 0;
}

.navbar-default .navbar-nav>li>a {
    font-size: 16px;
    color: #444;
    height: 70px;
    line-height: 35px;
}

.navbar-default .navbar-nav>li>a:hover {
    color: rgb(247, 46, 123);
}

.navbar-toggle {
    margin-top: 17px;
}

```
".navbar"设置导航栏的外边距为0，下边框为1像素的灰色实线。

".navbar-default"设置导航栏的背景颜色为白色。

".navbar-default .navbar-brand"设置导航栏中的网站标志的字体大小为30像素，加粗，高度为70像素，行高为35像素，内边距为0。

".navbar-default .navbar-nav>li>a"设置导航栏中每个链接的字体大小为16像素，颜色为#444（深灰色），高度为70像素，行高为35像素。

".navbar-default .navbar-nav>li>a:hover"设置导航栏中每个链接在鼠标悬停时的颜色为rgb(247, 46, 123)（粉红色）。

".navbar-toggle"设置导航栏中的菜单按钮的顶部外边距为17像素。

<font color="gree">遇到的问题及解决办法：</font><br>

>其实一开始没有那个播放音乐那一栏，但是导航栏右边有点空，我想起来这个动漫的背景音乐挺好听的，就百度了一下给HTML网页加播放音乐控件的语句。所以我就加了一个这个播放音乐的"audio"标签，但是我感觉这个很容易被忽略，所以我又百度了一下如何进入网页就自动播放。在标签里加入autoplay="autoplay"，解决了这个问题。
-------------------------
2.主页
```html
   <!--home-->
    <section id="home">
        <div class="jumbotron banner">
            <div class="container">
                <h1>罗小黑战记</h1>
                <p>《罗小黑战记》是木头（昵称MTJJ）及其工作室“寒木春华动画”制作的中国网络动画、动画电影、番外漫画系列作品，目前仍然在持续更新中。TV版网络动画于2011年3月17日至2019年8月27日发布第1至28话，第29至40话发布于2021年4月24日至2021年7月17日，之后将投入为期三年的第二部大电影的工作中。番外漫画《蓝溪镇》于2018年9月27日开始连载，讲述老君、清凝仙子与玄离的故事。</p>
           
            </div>
        </div>
    </section>
    <!--home-->

   
}

```

```css
 .banner {
    text-align: center;
    color: #fff;
    background: url(/images/luo.png);
    background-size: 100% 100%;
 }
```
“section”标签定义了一个名为“home”的页面区块，用于在页面上标识这个区块的作用。

“jumbotron”定义了一个大型的顶部区块，通常用于显示网站的主要信息或吸引用户的注意力。

“banner”定义了这个顶部区块的样式，可能包括背景图像、文本和其他元素。

“container”定义了这个顶部区块的容器，用于对其中的内容进行居中对齐和边距控制。

“h1”标签定义了一个标题级别为1的标题，用于显示“罗小黑战记”这个网站的主题。

“p”标签定义了一个段落，用于显示网站的描述。其中包括了《罗小黑战记》的制作方和年份，以及该系列作品的类型和当前状态。

<font color="gree">遇到的问题及解决办法：</font><br>
>这里我想的是需要一个醒目的图片用于放置这一段很长，有些枯燥的介绍的话，<br>但是我在网上找的图片一旦放进这个banner里图片就会变得很糊很不好看,然后我在网页上搜索到了Bigjpg这个工具,可以直接在网页上将图片无损放大，还可以使其变得更加清晰,<br>我还想在这个图片的基础上做一个延伸，所以我用电脑中自带的画图软件中的取色器提取出这张图片的主要背景颜色,自己做了一张纯色的图片，然后用美图秀秀把这两张图拼起来，最后呈现的这张图片就比较清晰，而且展示文字也不至于太花了。
----------------------------
3.人物卡片

```html
<section id="bbs">
        <div class="container">
            <div class="row fadeInUp">
                <div class="col-md-4">    
                        <img src="https://www.nitutu.com/uploads/allimg/191230/9c028cad1a9d4fceb702b44d7bb361a1.jpg"
                            class="img-responsive" alt="点击播放视频" id="thumbnail" title="点击播放视频">
                            <div id="videoModal" class="modal">
                                <video width="80%" height="80%" controls id="videoPlayer">
                                  <source src="song/vi1.mp4" type="video/mp4">  
                                </video>
                            </div>
                        <h3>罗小黑</h3>
                        <p>罗小黑诞生在2011年，是主角，原型是导演曾养过的一只黑猫 [7]。
                            原名小黑，遇见罗小白后由罗小白取名为“罗小黑”。师从无限，不会识字。因盗取老君天明珠而被谛听打回原形。躲入纸箱中避雨误被小白捡回家，取名罗小黑。尾巴是身长的两倍，可变成翅膀，也可分裂成名为嘿咻的有意识体，随着小黑能力越强，嘿咻也会越多，现可分裂为四个，也可以无限分裂，但总体积不变。是罕见的双灵质空间体质。</p>          
                </div>


    <style>
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0, 0, 0, 0.8);
          }
          
          .modal-display {
            display: flex;
            justify-content: center;
            align-items: center;
          }
        </style>
```
```css
#bbs {
    padding: 80px 0;
    text-align: center;
}

#bbs .col-md-4 {
    padding: 15px;
}

#bbs .col-md-4:hover {
    background: #f1f1f1;
    box-shadow: 1px 1px 4px #ccc;

}

#bbs a {
    color: #212121;
    text-decoration: none;
}

#bbs img {
    margin: 0 auto;
}

```
```javascript
 document.addEventListener("DOMContentLoaded", function () {
                const thumbnail = document.getElementById("thumbnail");
                const videoModal = document.getElementById("videoModal");
                const videoPlayer = document.getElementById("videoPlayer");
 // 点击图片显示视频模态框
                thumbnail.addEventListener("click", function () {
                  videoModal.classList.add("modal-display");
                  videoPlayer.play();
                });
              
                // 点击模态框外部区域关闭视频模态框
                videoModal.addEventListener("click", function (event) {
                  if (event.target === videoModal) {
                    videoPlayer.pause();
                    videoModal.classList.remove("modal-display");
                  }
                });
 }
```
“section”标签定义了一个名为“bbs”的页面区块，用于在页面上标识这个区块的作用。

“container”定义了这个页面区块的容器，用于对其中的内容进行居中对齐和边距控制。

“row”定义了这个页面区块的行，用于将其中的内容分为多列布局。

“col-md-4”定义了这个页面区块的列，用于将其中的内容占据页面宽度的四分之一。通常用于显示图片和文字描述。

“img”标签定义了一个图片，用于显示罗小黑的照片。其中的“src”属性指定了图片的来源，而“class”属性定义了图片的响应式样式，以适应不同大小的屏幕。

“h3”标签定义了一个标题级别为3的标题，用于显示罗小黑的名称。

“p”标签定义了一个段落，用于显示罗小黑的描述。其中包括了罗小黑的诞生时间、原名、属性、能力和经历等信息。

“video”标签定义了一个视频，用于在点击图片后显示罗小黑的视频。其中的“source”标签指定了视频的来源和格式，而“controls”属性用于添加视频播放控件。

“div”标签定义了一个模态框，用于在视频播放时弹出。其中的“id”属性用于标识这个模态框，而“class”属性定义了模态框的样式。

“#bbs”选择器设置了名为“bbs”的页面区块的样式。其中的“padding”属性用于设置区块的上下内边距为80像素，左右内边距为0，而“text-align”属性用于将区块中的文本居中对齐。

“#bbs .col-md-4”选择器设置了名为“col-md-4”的列的样式，用于将其中的内容进行内边距控制。其中的“padding”属性用于设置列的内边距为15像素，以增加内容的间距。

“#bbs .col-md-4:hover”选择器设置了名为“col-md-4”的列在鼠标悬停时的样式。其中的“background”属性用于设置列的背景色为#f1f1f1，以增加鼠标悬停时的视觉效果；而“box-shadow”属性用于添加列的阴影效果，以增加立体感。

“#bbs a”选择器设置了所有链接的样式。其中的“color”属性用于设置链接的文本颜色为#212121，即深灰色；而“text-decoration”属性用于去除链接的下划线，以避免视觉干扰。

“#bbs img”选择器设置了所有图片的样式。其中的“margin”属性用于将图片水平居中对齐，以增加页面的美观性。

<font color="gree">遇到的问题及解决办法：</font><br>

>添加的视频自己去b站录制的，使用csdn上面别人记录的自己在图片上添加视频文件的办法。失败而且看起来很难看过后，询问了某个人工智能聊天网页，让我了解到了视频模态框的用法，最后写出了还算比较好看的视频播放页面，添加了图片的title属性使得悬停在某个人物卡片上就会出现提示：点击可播放视频。
--------------------------
4.其他页面
```html
 <!--history-->
    <section id="history">
        <div class="container">
            <div class="col-md-7">
                <h2>历史</h2>
                <p>所有资料来源互联网</p>
                <p><span
                        class="glyphicon glyphicon-grain mai-icon"></span>MTJJ于2010年创作了罗小黑形象，次年03月17日推出了《罗小黑战记》<br>2011年4月开通官方微博@罗小黑CAT， 并开始连载罗小黑漫画及动画，形象于同年3月正式设定成熟。<br>
                </p>
                <p><span
                        class="glyphicon glyphicon-grain mai-icon"></span>2012年3月，罗小黑工作室变身为北京寒木春华动画技术有限公司，以运营国内原创动漫形象罗小黑为主。业务主要涵盖漫画创作及动画创作，动漫形象周边产品设计与销售。<br>电影版《罗小黑战记：不再流浪（我选择的未来）》于2019年9月7日上映。电影为动画的前传。
                </p>
            </div>
            <div class="col-md-5">
                <img src="https://www.dongmanzx.com/wp-content/uploads/2018/07/2018073114265750.jpg"
                    class="img-responsive" alt="" />
            </div>
        </div>
    </section>
    <!--history-->
```
“section”标签定义了一个名为“history”的页面区块，用于在页面上标识这个区块的作用。

“container”定义了这个页面区块的容器，用于对其中的内容进行居中对齐和边距控制。

“col-md-7”和“col-md-5”定义了这个页面区块中两列的布局。其中，“col-md-7”占据了宽度的7/12，用于显示历史文字信息；而“col-md-5”占据了宽度的5/12，用于显示历史图片信息。

“h2”标签定义了一个标题级别为2的标题，用于显示“历史”二字。

“p”标签定义了一个段落，用于显示罗小黑历史的文字描述。其中包括了罗小黑形象的创作时间、推出时间、官方微博开通时间，以及罗小黑工作室的发展历程和业务范围等信息。

“span”标签定义了一个内联元素，用于显示一个小麦粒图标。

“img”标签定义了一个图片，用于显示罗小黑历史的图片信息。其中的“src”属性指定了图片的来源，而“class”属性定义了图片的响应式样式，以适应不同大小的屏幕。
```html
 <!--contact-->
    <section id="contact">
        <div class="lvjing">
            <div class="container">
                <div class="row">
                    <div class="col-md-7">
                        <h2>
                            联系我们
                        </h2>
                        <p>
                            猫妖小黑盗取天明珠被谛听发现，被打回原形重伤而逃，在流落街头之时被罗小白带回了家，起名罗小黑。有一天小黑突然变成了人形，告诉小白自己要暂时离开去完成师父交给自己的任务。却在离开之后因为师傅交给自己的任务又回到了小白身边，等待着他们的会是什么呢…… ----众生之门篇 
                            罗小黑不是一只普通的猫咪，它极通人性，会蹲马桶，不吃猫粮，长长的尾巴甚至能分裂成多个名为“黑咻”的生物体。另一方面，谛听发动手下三匹长着翅膀的狼，搜寻着罗小黑的下落。不久，罗小白带着小黑到乡下探望堂哥阿根和爷爷，由此发生了种种离奇玄幻事件。
                            故事就这样开始了…
                        </p>
                        <address>
                            <p> 
                                地址: MTJJ木头的工作室
                            </p>
                            <p>   
                                微博：<a href="https://www.weibo.com/luoxiaohei">罗小黑的微博</a>
                            </p>
                            <p>
                                观看地址：<a href="https://www.bilibili.com/bangumi/play/ss1733?spm_id_from=333.337.0.0">b站 罗小黑战记</a>
                            </p>
                        </address>
                    </div>
                    <div class="col-md-5">
                        <img align="right"
                            src="https://www.taoshudang.com/wp-content/uploads/2019/10/s28156108.jpg"
                            class="img-responsive" />
                    </div>
                </div>
            </div>
        </div>
    </section>
    <!--contact-->  
```
“section”标签定义了一个名为“contact”的页面区块，用于在页面上标识这个区块的作用。

“container”定义了这个页面区块的容器，用于对其中的内容进行居中对齐和边距控制。

“row”定义了这个页面区块中的行，用于将其中的内容排列成一行两列的格式。

“col-md-7”和“col-md-5”定义了这个页面区块中两列的布局。其中，“col-md-7”占据了宽度的7/12，用于显示联系方式和简介的文字信息；而“col-md-5”占据了宽度的5/12，用于显示联系方式和简介的图片信息。

“h2”标签定义了一个标题级别为2的标题，用于显示“联系我们”四个字。

“p”标签定义了一个段落，用于显示罗小黑的简介和故事背景。其中包括了罗小黑的成长历程、不同寻常的特点，以及故事的开端和发展情节等信息。

“address”标签定义了一个联系地址的区块，用于显示联系方式。其中包括了MTJJ木头的工作室地址、罗小黑的微博链接和观看罗小黑战记的B站链接等信息。

“a”标签定义了一个超链接，用于跳转到罗小黑的微博或观看罗小黑战记的B站链接。

“img”标签定义了一个图片，用于显示罗小黑联系方式和简介的图片信息。其中的“src”属性指定了图片的来源，而“class”属性定义了图片的响应式样式，以适应不同大小的屏幕。

```css
/*contact*/
#contact {
    background: url("https://img.zcool.cn/community/01f9075e58f4fda80120a8950afc77.jpg@3000w_1l_2o_100sh.jpg") no-repeat;
    background-size: cover;
    color: #ffffff;
}

#contact h2 {
    font-weight: bold;
    margin-top: 0;
    margin-bottom: 25px;
}

#contact p {
    line-height: 24px;
    margin-bottom: 2px;
}

```
“#contact”选择器用于选择样式将应用于ID为“contact”的页面区块。

“background”属性定义了页面区块的背景图片，其中的URL指定了图片的来源。而“no-repeat”和“background-size: cover”属性用于设置图片的重复方式和尺寸。

“color”属性定义了页面区块中文字的颜色为白色。

“h2”选择器用于选择样式将应用于页面区块中的标题级别为2的标题。

“font-weight”属性定义了标题的字体加粗程度为粗体。

“margin-top”和“margin-bottom”属性分别定义了标题上方和下方的外边距大小，用于控制标题和其他元素之间的垂直间距。

“p”选择器用于选择样式将应用于页面区块中的段落。

“line-height”属性定义了段落的行高，用于控制段落中每行文字之间的垂直间距。

“margin-bottom”属性定义了段落下方的外边距大小，用于控制段落和其他元素之间的垂直间距。

<font color="blue">仍未解决的问题：</font><br>

>导航栏的音乐播放仍然存在时而自动播放，时而不会自动播放，而且在播放视频时音乐不会自动暂停，需要手动暂停。

<font color="pink">收获：</font><br>
夹带私货的感觉真是太好啦（bushi）！宣传自己喜欢的动漫真的很开心！而且还收获了使用bootstrap.min.css的一些样式的经验！在搜索过程中也看到了许多优秀的网页设计，使我对html和css的知识更加熟练运用了。

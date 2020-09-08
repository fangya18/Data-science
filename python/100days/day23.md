
## Day 23
### Ex1. Yoko Kitchen

<!DOCTYPE html>
<html>
	<head>
		<title>HTML5 Layout</title>
		<style type="text/css">
			header,
			section,
			footer,
			aside,
			nav,
			article,
			figure,
			figcaption {
				display: block;
			}

			body {
				color: #666666;
				background-color: #f9f8f6;
				background-image: url("images/dark-wood.jpg");
				background-position: center;
				font-family: Georgia, Times, serif;
				line-height: 1.4em;
				margin: 0px;
			}

			.wrapper {
				width: 940px;
				margin: 20px auto 20px auto;
				border: 2px solid #000000;
				background-color: #ffffff;
			}

			header {
				height: 160px;
				background-image: url(images/header.jpg);
			}

			h1 {
				text-indent: -9999px;
				width: 940px;
				height: 130px;
				margin: 0px;
			}

			nav,
			footer {
				clear: both;
				color: #ffffff;
				background-color: #aeaca8;
				height: 30px;
			}

			nav ul {
				margin: 0px;
				padding: 5px 0px 5px 30px;
			}

			nav li {
				display: inline;
				margin-right: 40px;
			}

			nav li a {
				color: #ffffff;
			}

			nav li a:hover,
			nav li a.current {
				color: #000000;
			}

			section.courses {
				float: left;
				width: 659px;
				border-right: 1px solid #eeeeee;
			}

			article {
				clear: both;
				overflow: auto;
				width: 100%;
			}

			hgroup {
				margin-top: 40px;
			}

			figure {
				float: left;
				width: 290px;
				height: 220px;
				padding: 5px;
				margin: 20px;
				border: 1px solid #eeeeee;
			}

			figcaption {
				font-size: 90%;
				text-align: left;
			}

			aside {
				width: 230px;
				float: left;
				padding: 0px 0px 0px 20px;
			}

			aside section a {
				display: block;
				padding: 10px;
				border-bottom: 1px solid #eeeeee;
			}

			aside section a:hover {
				color: #985d6a;
				background-color: #efefef;
			}

			a {
				color: #de6581;
				text-decoration: none;
			}

			h1,
			h2,
			h3 {
				font-weight: normal;
			}

			h2 {
				margin: 10px 0px 5px 0px;
				padding: 0px;
			}

			h3 {
				margin: 0px 0px 10px 0px;
				color: #de6581;
			}

			aside h2 {
				padding: 30px 0px 10px 0px;
				color: #de6581;
			}

			footer {
				font-size: 80%;
				padding: 7px 0px 0px 20px;
			}
		</style>
		<!--[if lt IE 9]>
		<script src="http://html5shiv.googlecode.com/svn/trunk/html5.js"></script>
		<![endif]-->
	</head>
	<body>
		<div class="wrapper">
			<header>
				<h1>Yoko's Kitchen</h1>
				<nav>
					<ul>
						<li><a href="" class="current">home</a></li>
						<li><a href="">classes</a></li>
						<li><a href="">catering</a></li>
						<li><a href="">about</a></li>
						<li><a href="">contact</a></li>
					</ul>
				</nav>
			</header>
			<section class="courses">
				<article>
					<figure>
						<img src="images/bok-choi.jpg" alt="Bok Choi" />
						<figcaption>Bok Choi</figcaption>
					</figure>
					<hgroup>
						<h2>Japanese Vegetarian</h2>
						<h3>Five week course in London</h3>
					</hgroup>
					<p>
						A five week introduction to traditional Japanese vegetarian meals, teaching you a selection of rice and noodle
						dishes.
					</p>
				</article>
				<article>
					<figure>
						<img src="images/teriyaki.jpg" alt="Teriyaki sauce">
						<figcaption>Teriyaki Sauce</figcaption>
					</figure>
					<hgroup>
						<h2>Sauces Masterclass</h2>
						<h3>One day workshop</h3>
					</hgroup>
					<p>
						An intensive one-day course looking at how to create the most delicious sauces for use in a range of Japanese
						cookery.
					</p>
				</article>
			</section>
			<aside>
				<section class="popular-recipes">
					<h2>Popular Recipes</h2>
					<a href="">Yakitori (grilled chicken)</a>
					<a href="">Tsukune (minced chicken patties)</a>
					<a href="">Okonomiyaki (savory pancakes)</a>
					<a href="">Mizutaki (chicken stew)</a>
				</section>
				<section class="contact-details">
					<h2>Contact</h2>
					<p>
						Yoko's Kitchen<br>
						27 Redchurch Street<br>
						Shoreditch<br>
						London E2 7DP
					</p>
				</section>
			</aside>
			<footer>
				&copy; 2011 Yoko's Kitchen
			</footer>
		</div>
	</body>
</html>


```python
####code
```


```python
<!DOCTYPE html>
<html>
	<head>
		<title>HTML5 Layout</title>
		<style type="text/css">
			header,
			section,
			footer,
			aside,
			nav,
			article,
			figure,
			figcaption {
				display: block;
			}

			body {
				color: #666666;
				background-color: #f9f8f6;
				background-image: url("images/dark-wood.jpg");
				background-position: center;
				font-family: Georgia, Times, serif;
				line-height: 1.4em;
				margin: 0px;
			}

			.wrapper {
				width: 940px;
				margin: 20px auto 20px auto;
				border: 2px solid #000000;
				background-color: #ffffff;
			}

			header {
				height: 160px;
				background-image: url(images/header.jpg);
			}

			h1 {
				text-indent: -9999px;
				width: 940px;
				height: 130px;
				margin: 0px;
			}

			nav,
			footer {
				clear: both;
				color: #ffffff;
				background-color: #aeaca8;
				height: 30px;
			}

			nav ul {
				margin: 0px;
				padding: 5px 0px 5px 30px;
			}

			nav li {
				display: inline;
				margin-right: 40px;
			}

			nav li a {
				color: #ffffff;
			}

			nav li a:hover,
			nav li a.current {
				color: #000000;
			}

			section.courses {
				float: left;
				width: 659px;
				border-right: 1px solid #eeeeee;
			}

			article {
				clear: both;
				overflow: auto;
				width: 100%;
			}

			hgroup {
				margin-top: 40px;
			}

			figure {
				float: left;
				width: 290px;
				height: 220px;
				padding: 5px;
				margin: 20px;
				border: 1px solid #eeeeee;
			}

			figcaption {
				font-size: 90%;
				text-align: left;
			}

			aside {
				width: 230px;
				float: left;
				padding: 0px 0px 0px 20px;
			}

			aside section a {
				display: block;
				padding: 10px;
				border-bottom: 1px solid #eeeeee;
			}

			aside section a:hover {
				color: #985d6a;
				background-color: #efefef;
			}

			a {
				color: #de6581;
				text-decoration: none;
			}

			h1,
			h2,
			h3 {
				font-weight: normal;
			}

			h2 {
				margin: 10px 0px 5px 0px;
				padding: 0px;
			}

			h3 {
				margin: 0px 0px 10px 0px;
				color: #de6581;
			}

			aside h2 {
				padding: 30px 0px 10px 0px;
				color: #de6581;
			}

			footer {
				font-size: 80%;
				padding: 7px 0px 0px 20px;
			}
		</style>
		<!--[if lt IE 9]>
		<script src="http://html5shiv.googlecode.com/svn/trunk/html5.js"></script>
		<![endif]-->
	</head>
	<body>
		<div class="wrapper">
			<header>
				<h1>Yoko's Kitchen</h1>
				<nav>
					<ul>
						<li><a href="" class="current">home</a></li>
						<li><a href="">classes</a></li>
						<li><a href="">catering</a></li>
						<li><a href="">about</a></li>
						<li><a href="">contact</a></li>
					</ul>
				</nav>
			</header>
			<section class="courses">
				<article>
					<figure>
						<img src="images/bok-choi.jpg" alt="Bok Choi" />
						<figcaption>Bok Choi</figcaption>
					</figure>
					<hgroup>
						<h2>Japanese Vegetarian</h2>
						<h3>Five week course in London</h3>
					</hgroup>
					<p>
						A five week introduction to traditional Japanese vegetarian meals, teaching you a selection of rice and noodle
						dishes.
					</p>
				</article>
				<article>
					<figure>
						<img src="images/teriyaki.jpg" alt="Teriyaki sauce">
						<figcaption>Teriyaki Sauce</figcaption>
					</figure>
					<hgroup>
						<h2>Sauces Masterclass</h2>
						<h3>One day workshop</h3>
					</hgroup>
					<p>
						An intensive one-day course looking at how to create the most delicious sauces for use in a range of Japanese
						cookery.
					</p>
				</article>
			</section>
			<aside>
				<section class="popular-recipes">
					<h2>Popular Recipes</h2>
					<a href="">Yakitori (grilled chicken)</a>
					<a href="">Tsukune (minced chicken patties)</a>
					<a href="">Okonomiyaki (savory pancakes)</a>
					<a href="">Mizutaki (chicken stew)</a>
				</section>
				<section class="contact-details">
					<h2>Contact</h2>
					<p>
						Yoko's Kitchen<br>
						27 Redchurch Street<br>
						Shoreditch<br>
						London E2 7DP
					</p>
				</section>
			</aside>
			<footer>
				&copy; 2011 Yoko's Kitchen
			</footer>
		</div>
	</body>
</html>
```

#### Ex2. Coffee Bar Example

<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>锚点连接</title>
	<style>
		h1 {
			margin-left: 100px
		}
		p {
			margin: 40px 120px;
		}
		#adv {
			width: 200px;
			height: 200px;
			color: yellow;
			background-color: rgba(0, 0, 255, 0.75);
			/* background-color: blue; */
			/* opacity: 0.5; */
			position: fixed;
			right: 50px;
			top: 20px;
		}
		/* position属性的取值 */
		/* 1. static - 静态定位 - 正常的文档流 */
		/* 2. relative - 相对定位 - 相对于原来正常的位置 */
		/* 3. absolute - 绝对定位 - 相对于父元素来设置位置 */
		/* 4. fixed - 固定定位 - 相对于浏览器窗口来设置位置 */
	</style>
</head>
<body>
	<div id="adv">
		For Rent
		<button id="closeBtn" style="float: right;">关闭</button>
	</div>
	<h1>Sin/Cos Coffee Bar</h1>
	<hr>
	<p>
	Milk tea
	</p>
	<p class="p2">
	Cookies
	</p>
	<p>
	Bubble tea
	</p>
	<p>
	Tea
	</p>
	<p>
	Bread
	</p>
	<a name="bar"></a>
	<p>
	Cake
	</p>
	<p>
	Ice-cream
	</p>
	<a name="foo"></a>
	<a href="javascript:history.back()">返回</a>
	<p>
    Coffee
	</p>
	<script>
		var closeBtn = document.getElementById('closeBtn')
		closeBtn.addEventListener('click', function () {
			// var advDiv = document.getElementById('adv')
			// advDiv.style.display = 'none'
			location.href = 'http://youku.com'
		})
	</script>
</body>
</html>


```python
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>锚点连接</title>
	<style>
		h1 {
			margin-left: 100px
		}
		p {
			margin: 40px 120px;
		}
		#adv {
			width: 200px;
			height: 200px;
			color: yellow;
			background-color: rgba(0, 0, 255, 0.75);
			/* background-color: blue; */
			/* opacity: 0.5; */
			position: fixed;
			right: 50px;
			top: 20px;
		}
		/* position属性的取值 */
		/* 1. static - 静态定位 - 正常的文档流 */
		/* 2. relative - 相对定位 - 相对于原来正常的位置 */
		/* 3. absolute - 绝对定位 - 相对于父元素来设置位置 */
		/* 4. fixed - 固定定位 - 相对于浏览器窗口来设置位置 */
	</style>
</head>
<body>
	<div id="adv">
		For Rent
		<button id="closeBtn" style="float: right;">关闭</button>
	</div>
	<h1>Sin/Cos Coffee Bar</h1>
	<hr>
	<p>
	Milk tea
	</p>
	<p class="p2">
	Cookies
	</p>
	<p>
	Bubble tea
	</p>
	<p>
	Tea
	</p>
	<p>
	Bread
	</p>
	<a name="bar"></a>
	<p>
	Cake
	</p>
	<p>
	Ice-cream
	</p>
	<a name="foo"></a>
	<a href="javascript:history.back()">返回</a>
	<p>
    Coffee
	</p>
	<script>
		var closeBtn = document.getElementById('closeBtn')
		closeBtn.addEventListener('click', function () {
			// var advDiv = document.getElementById('adv')
			// advDiv.style.display = 'none'
			location.href = 'http://youku.com'
		})
	</script>
</body>
</html>
```

#### Ex3. HTMl Video/Audio

<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>Audio Video</title>
	</head>
	<body>
		<audio controls autoplay loop>
			<source src="audio/test-audio.mp3"></source>
		</audio>
		<video width="400" controls>
			<source src="video/puppy.mp4"></source>
		</video>
	</body>
</html>


```python
#### Code
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>Audio Video</title>
	</head>
	<body>
		<audio controls autoplay loop>
			<source src="audio/test-audio.mp3"></source>
		</audio>
		<video width="400" controls>
			<source src="video/puppy.mp4"></source>
		</video>
	</body>
</html>
```

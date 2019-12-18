## 18/12

```
// create toilet project using addEventListener to click the button to do sth
//html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Document</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <div class="tank">
      <div style="background-color:lightgray;" , class="flush-btn"></div>
    </div>
    <div class="bowl"></div>
    <script src="app.js"></script>
  </body>
</html>

//css

* {
  box-sizing: border-box;
}
/* "*" to apply all element */

body {
  background-color: grey;
}
.tank {
  background-color: white;
  width: 400px;
  height: 200px;
  border-radius: 30px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.bowl {
  transition: all linear 400ms;
  background-color: rgb(71, 131, 71);
  width: 400px;
  height: 400px;
  border-radius: 20% 20% 40% 40%;
  /* topleft topright bottomright bottomleft */
  border: 60px solid white;
  padding: 20px;
  box-shadow: inset 0 0 20px grey;
}
.flush-btn {
  width: 200px;
  height: 100px;
  box-shadow: 0 4px 8px 0 grey;
  cursor: pointer;
  text-align: center;
}

//app.js
var bowl = document.querySelector(".bowl");
var flush1 = document.querySelector(".flush-btn");
var poop = function() {
  window.document.body.children[1].style.backgroundColor = "darkolivegree";
};

var flush = function() {
  window.document.body.children[1].style.backgroundColor = "mintcream";
};
// window.document.body.children[1].addEventListener("click", poop);
// window.document.body.children[0].children[0].addEventListener("click", flush);
bowl.addEventListener("click", poop);
flush1.addEventListener("click", flush);

```
```
//crappy calculation to calculate 2 numbers and submit to get value

//html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=<device-width>, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Document</title>
  </head>
  <body>
    <h1>crappy calculator</h1>
    <input class="number1" type="number" value="number" /> +
    <input class="number2" type="number" value="number" />
    <span>?</span>
    <button class="submit-btn">submit</button>
    <script src="app.js"></script>
  </body>
</html>

//css
var num1 = document.querySelector(".number1");
var num2 = document.querySelector(".number2");
var span = document.querySelector("span");
var submitBtn = document.querySelector(".submit-btn");
//Event handler
var handleClick = function() {
  var sum = Number(num1.value) + Number(num2.value);
  //input when print is a string ,need to convert using Number
  span.textContent = sum;
};

submitBtn.addEventListener("click", handleClick);

```
```
//fashion-css project
file:///Users/gloriachen/sei/code-alongs/02-web/fashion_css/index.html

//html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Document</title>
    <link rel="stylesheet" href="css/style.css" />
  </head>
  <body>
    <header>
      <h2><span class="title">Sartre's List</span> Better-Dressed People</h2>
      <nav>
        <ul class="headnav">
          <li><a href="">Women's</a></li>
          <li><a href="">Men's</a></li>
          <li><a href="">On the Street</a></li>
          <li><a href="">The Catwalk</a></li>
          <li><a href="">AdWatch</a></li>
          <li><a href="">About</a></li>
        </ul>
        <!-- can only use a tag 
        ul>li*6 {item}-->
      </nav>
    </header>
    <div class="container">
      <main>
        <article>
          <p>11/12/13</p>
          <p>On the street in Brooklyn</p>
          <img src="images/fashion_photo.jpeg" alt="" />
          <p>
            <span class="firstletter">C</span>ray culpa stuptown,flexitarian ex
            odd Future do fugiat Wes Anderson proident 3 wolf moon officia
            bitter small batch.
            <a href="" class="link">Continues...</a>
          </p>
        </article>
        <article>
          <p>11/11/13</p>
          <img src="images/fashion_photo2.jpeg" alt="" />
          <p>
            <span class="firstletter">S</span>elfies sunt Tumblr, delectus small
            batch DIY umanmi sint.Polaroid chambray selfies McSeeney's Cosby
            sweater.
            <a href="" class="link">Continues...</a>
          </p>
        </article>
      </main>
      <aside>
        <section>
          <h3>About Us</h3>
          <p>
            Sartre's List is u salvia, fixie mumblecore ex aesthetic qui minim
            blog cliche.retro disrupt keytar PBR, delectus consetetur
            flexitarian fingerstache selfies nostrud Schitz.<a
              href=""
              class="link"
              >More...</a
            >
          </p>
        </section>
        <section class="ad"><span class="adword">Ad</span></section>
        <section>
          <h3>Popular Posts</h3>
          <ul class="post">
            <li>10 Things Not to Wear on the Red Carpet</li>
            <li>Valhalla at The Met Gala</li>
            <li>Jeans: To Fray or Not to Fray</li>
            <li>"Trashion" is in This Season</li>
            <li>Back to School in Pencil Skirts</li>
            <li>Fall Season Preview</li>
            <li>Even more Ways to Wrap a Sari!</li>
            <li>Is Steam Punk Here to Stay?</li>
            <li>Neighborhoodie Watch</li>
            <li>Hair Styles of the Damned</li>
          </ul>
        </section>
      </aside>
    </div>
    <footer>
      <nav>
        <ul class="tailnav">
          <li><a href="">Home</a></li>
          <li><a href="">Women's</a></li>
          <li><a href="">Men's</a></li>
          <li><a href="">On the Street</a></li>
          <li><a href="">The Catwalk</a></li>
          <li><a href="">AdWatch</a></li>
          <li><a href="">About</a></li>
          <li><a href="">Tips</a></li>
        </ul>
      </nav>
      <p class="copyright">@copy; 2013 Valet Industries, Inc</p>
    </footer>
  </body>
</html>


//css
body {
  color: grey;
}
h2 {
  font-weight: 300;
}
.title {
  color: rgb(216, 46, 46);
  font-size: 40px;
}
.container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-gap: 15px;
  width: 100%;
  margin: 0 auto;
}
.headnav {
  display: flex;
  align-items: center;
  justify-content: space-around;
  list-style-type: none;
  text-align: center;
}
.headnav li {
  flex: 1;
  /* flex-grow: 1; * same result*/
  background-color: black;
  /* margin-right: 2px; */
  line-height: 60px;
  font-size: 17px;
  border-right: 1px solid #bbb;
}
.headnav li a {
  color: #bbb;
  text-decoration: none;
}
li:last-child {
  border-right: none;
}
.tailnav {
  display: flex;
  align-items: center;
  /* justify-content: space-around; */
  padding: 2px;
  list-style-type: none;
  text-align: center;
}
.tailnav li {
  justify-content: flex-start;
  /* flex: 1; */
  background-color: white;
  line-height: 40px;
  /*font-size: 17px; */
  border-left: 1px solid #bbb;
  margin-right: 10px;
}
.tailnav li a {
  color: rgb(240, 96, 96);
  text-decoration: none;
  margin-right: 2px;
}
.tailnav ul li first-child {
  border-left: none;
}
.firstletter {
  font-size: 60px;
  color: rgb(163, 154, 154);
}
/* p::first-letter{color: red; float:left;font-size:80px;} */
.link {
  color: red;
  font-weight: bold;
  font-size: 20px;
}
article {
  border-bottom: 1px solid grey;
}
aside {
  /* flex-direction: column; */
  display: grid;
  grid-template-rows: 1fr 1fr 1fr;
}
.ad {
  background-color: rgb(197, 184, 184);
}
.adword {
  font-size: 200px;
  display: block;
  text-align: center;
  margin: 0 auto;
}
.post {
  color: rgb(241, 78, 78);
}
.copyright {
  font-size: 20px;
}

```
## 17/12
```
//html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Document</title>
    <link rel="stylesheet" href="css/style.css" />
  </head>
  <body>
    <header>
      <img src="images/logo.png" alt="" class="logo" />
    </header>
    <div class="container">
      <main class="startup">
        <article>
          <h2>Ecard of the Day</h2>
          <img src="images/ecard-nycstartups.jpg" alt="" />
          <p>
            Lorem ipsum dokir sit amet,consectetur adipiccubg elit.Vivamus
            aliquet vulputate varius.<a href="">DOWNLOAD</a>
          </p>
          <footer>
            Post by <span>Steve Smith</span> on August 2, 2012/Comments
            (<span>3</span>)
          </footer>
        </article>
        <article>
          <h2>Doing The Big work</h2>
          <img src="images/ecard-courage.jpg" alt="" />
          <p>
            Lorem ipsum dokir sit amet,consectetur adipiccubg elit.Vivamus
            aliquet vulputate varius.<a href="">DOWNLOAD</a>
          </p>
          <footer>
            Post by <span>Steve Smith</span> on August 2, 2012/Comments
            (<span>3</span>)
          </footer>
        </article>
      </main>
      <aside class="archive">
        <nav>
          <ul class="nav">
            <li>ARCHIIVE</li>
            <li>January</li>
            <li>February</li>
            <li>March</li>
            <li>April</li>
            <li>May</li>
            <li>June</li>
            <li>July</li>
          </ul>
        </nav>
        <nav>
          <ul class="nav">
            <li>BLOGROLL</li>
            <li>Mailchimp</li>
            <li>Shopify</li>
            <li>The Next Web</li>
            <li>Mint.com</li>
            <li>Mashable</li>
          </ul>
        </nav>
        <img src="images/ad-cut-and-paste.gif" alt="" />
        <img src="images/ad-postcard-tee.png" alt="" />
        <img src="images/ad-submit-your-own.png" alt="" />
      </aside>
    </div>
    <footer class="footer">
      <img src="images/social-icon-facebook.png" alt="" />
      <img src="images/social-icon-pinterest.png" alt="" />
      <img src="images/social-icon-twitter.png" alt="" />
    </footer>
  </body>
</html>


//css
body {
  background-color: rgb(206, 191, 191);
  background-image: url("../images/background.jpg");
  background-repeat: repeat-x;
}

.logo {
  display: block;
  margin: 0 auto;
} 
a {
  color: red;
  font-weight: bold;
}

.startup {
  background-color: white;
  margin: 0 auto;
  width: 100%;
}
.archive {
  background-color: white;
  margin: 0 auto;
  width: 100%;
}
span {
  color: red;
  font-weight: 700;
}
.container {
  display: grid;
  grid-template-columns: 2fr 1fr;
  grid-gap: 15px;
  width: 100%;
  margin: 0 auto;
}
.footer {
  display: flex;
  justify-content: center;
  width: 100%;
}
.nav {
  list-style-type: none;
  justify-content: center;
}
@media all and (min-width: 800px) {
  .container {
    width: 80%;
    margin: 0 auto;
  }
}

article footer {
  border-top: 1px dotted black;
  border-bottom: 1px solid black;
}
@media all and (max-width: 500px){
  .container {
    display: block;

  }

```

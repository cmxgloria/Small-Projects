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

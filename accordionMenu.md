```
//index.html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="style.css" />
    <title>Document</title>
  </head>
  <body>
    <h1>Accordion Menu</h1>

    <ul class="accordion">
      <li>
        <a class="toggle" href="javascript:void(0);">Web Design</a>
        <ul class="inner" style="display: none;">
          <li>
            <a href="#" class="toggle">Coding</a>
            <div class="inner">
              <p>JavaScript</p>
              <p>jQuery</p>
              <p>Ruby</p>
            </div>
          </li>
          <li>Devices</li>
          <li>Global</li>
        </ul>
      </li>
    </ul>

    <script src="https://code.jquery.com/jquery-1.12.4.js"></script>
    <script src="https://code.jquery.com/ui/1.12.1/jquery-ui.js"></script>
    <script src="accordionMenu.js"></script>
  </body>
</html>


//js
$(".toggle").click(function(e) {
  e.preventDefault();
  var $this = $(e.target);
  $this.next().slideToggle(350);
});
```

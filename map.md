```
//app.js
const results = [
  {
    name: "Melbourne Cricket Grounds",
    location: { lat: -37.819967, long: 144.983449 }
  },
  { name: "Flagstaff Gardens", location: { lat: -37.81068, long: 144.954352 } },
  {
    name: "Emporium Melbourne",
    location: { lat: -37.812433, long: 144.963787 }
  },
  { name: "City Library", location: { lat: -37.817039, long: 144.965983 } },
  {
    name: "Southern Cross Station",
    location: { lat: -37.818281, long: 144.952776 }
  },
  {
    name: "Sea Life Melbourne Aquarium",
    location: { lat: -37.82064, long: 144.958325 }
  }
];
// callback=GetMap from script in html
function GetMap() {
  console.log("khkh");
  // map id from div
  var map = new Microsoft.Maps.Map("#map", {
    center: new Microsoft.Maps.Location(-37.818555, 144.959076),
    zoom: 17
  });

  function addPin(result) {
    //Create custom Pushpin
    var pin = new Microsoft.Maps.Pushpin(
      { latitude: result.location.lat, longitude: result.location.long },
      {
        title: result.name,
        subTitle: "SEI",
        text: "1"
      }
    );
    //Add the pushpin to the map
    map.entities.push(pin);
  }
  results.forEach(addPin);
}

```
 
```
//index.html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Document</title>
    <link rel="stylesheet" href="style.css" />
    <!-- callback async script tag leave here, because not know when new script finish loading then run my script app.js -->
    <!-- Reference to the Bing Maps SDK -->
    <script
      type="text/javascript"
      src="http://www.bing.com/api/maps/mapcontrol?callback=GetMap&key=AtwX-4hMJnw40uObdVSKBMT-XsdRWAQZdAWRvPuoIBa2Ebr1lT8J3NKehbYwQzcs"
      async
      defer
    ></script>
  </head>
  <body>
    <div id="map"></div>
    <script src="app.js"></script>
  </body>
</html>

```

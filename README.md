<!DOCTYPE html>
<html>
<head>
    <meta charset='utf-8' />
    <title>City-Guesser</title>
    <meta name='viewport' content='initial-scale=1,maximum-scale=1,user-scalable=no' />
    <script src='https://api.tiles.mapbox.com/mapbox-gl-js/v0.42.2/mapbox-gl.js'></script>
    <!-- <script src='cities.geojson'></script> -->
    <script src='cities_nat_500k3s.geojson'></script>
<link href="https://fonts.googleapis.com/css?family=Josefin+Sans" rel="stylesheet">


    <link href='https://api.tiles.mapbox.com/mapbox-gl-js/v0.42.2/mapbox-gl.css' rel='stylesheet' />

    <style>
        body { margin:0; padding:0; background-color: #FCFAF2;}

        #wrapper {
          overflow: auto;
          /*position: fixed;*/
        }
        #map {
          top:0;
          bottom:0;
          width: calc(100% - 300px);
          height: 100vh;
          background-color: black;
          border-right: 1px solid darkgrey;
          float:left
        }
        #section {
          height: 100vh;
          width: 279px;
          overflow: auto;
          background-color: #FCFAF2;
          padding-left: 10px;
          padding-right: 10px;
        }
        input[type="submit"] {
          background: #FF8082;
          border: 1px solid;
          border-color: #FCFAF2;
          color: white;
          padding: 10px 15px;
          cursor: pointer;
          font-family: 'Josefin Sans', sans-serif;
        }
        h3 {
          font-family: 'Josefin Sans', sans-serif;
          font-size: 32px;
          display: inline;
        }
        p {
          display: inline;
          font-family: 'Josefin Sans', sans-serif;
        }

        #att {
          font-size: 12px;
          padding: 7px;
          border: 1px solid;
          border-color: lightgrey;
          background-color: #FCFAF2;
        }
        #att p {
          color: grey;
        }

        #att a {
          text-decoration: none;
          color: #444444;
        }



    </style>

</head>
<body>

<div id='wrapper'>

  <div id='map'></div>

  <div id='section'>
    <br>
    <form name="quizForm" onsubmit="return submitAnswers()">
          <h3>City-Guesser</h3>
          <!-- <br>
          <p>&nbsp;(a map-based quiz game)</p> -->
          <br><br>
          <p>&nbsp;Level: </p><p id="level">1</p><p>&nbsp;</p><br>
          <p>&nbsp;Score: </p><p id="score">0</p><br>
          <br>

          <input type="radio" name="q1" value="1" id="q1a"><p id="p1"></p><br>
          <input type="radio" name="q1" value="2" id="q1b"><p id="p2"></p><br>
          <input type="radio" name="q1" value="3" id="q1c"><p id="p3"></p><br>
          <input type="radio" name="q1" value="4" id="q1d"><p id="p4"></p><br>

          <br>
          <input type="submit" value="Submit Answer">
    </form>
    <br>

    <p>&nbsp;</p><p id="message">Good Luck!</p><br>
    <p id="code"></p>
    <br>
    <p>&nbsp;Max Level Achieved: </p><p id="hlevel">0</p><br>
    <p>&nbsp;High Score: </p><p id="hscore">0</p><br>

    <br>
    <br>

  <div id="att">
  <p>
    Source code for this map is on <a href="https://github.com/jamaps/city-guesser/"target="_blank">GitHub</a>.<br> It was designed and built by <a href="https://jamaps.github.io/"target="_blank">Jeff Allen</a> in 2017 using <a href="http://mapbox.com/"target="_blank">Mapbox</a> and <a href="https://www.qgis.org/en/site/"target="_blank">QGIS</a>, with data from <a href="http://openstreetmap.org/"target="_blank">OpenStreetMap</a> and <a href="http://www.naturalearthdata.com/"target="_blank">Natural Earth</a>.
  </p>

</div>

  <p><br></p>

  </div>

</div>

<script src='map_all.js'></script>

</body>
</html>

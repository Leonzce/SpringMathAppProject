Skycons
=======

[Preview them here](https://maxdow.github.io/skycons/)

Skycons is a set of twenty two animated weather glyphs, procedurally generated
by JavaScript using the HTML5 canvas tag. They're easy to use, and pretty
lightweight, so they shouldn't rain on your parade:

    <canvas id="icon1" width="128" height="128"></canvas>
    <canvas id="icon2" width="128" height="128"></canvas>

    <script>

      // by default, icons are black but you can color them
      var skycons = new Skycons({"color": "pink"});
      // on Android, a nasty hack is needed: {"resizeClear": true}

      // If you want to add more colors :
      // var skycons = new Skycons({"monochrome": false});
      // you can now customize the color of different parts
      // main, moon, fog, fogbank, light_cloud, cloud, dark_cloud,
      // thunder, snow, hail, sleet, wind, leaf, rain, sun
      // var skycons = new Skycons({
      //  "monochrome": false,
      //  "color" : {
      //    "cloud" : "#F00"
      //  }
      //  });


      // you can add a canvas by it's ID...
      skycons.add("icon1", Skycons.PARTLY_CLOUDY_DAY);

      // ...or by the canvas DOM element itself.
      skycons.add(document.getElementById("icon2"), Skycons.RAIN);

      // if you're using the Forecast API, you can also supply
      // strings: "partly-cloudy-day" or "rain".

      // start animation!
      skycons.play();

      // you can also halt animation with skycons.pause()

      // want to change the icon? no problem:
      skycons.set("icon1", Skycons.PARTLY_CLOUDY_NIGHT);

      // want to remove one altogether? no problem:
      skycons.remove("icon2");
    </script>

Skycons were designed for [Forecast](http://forecast.io/) by those wacky folks
at The Dark Sky Company, and were heavily inspired by Adam Whitcroft's
excellent [Climacons](http://adamwhitcroft.com/climacons/). The source code has
been [released into the public domain][cc0], so please do with it as you see
fit! ♡

[cc0]: http://creativecommons.org/publicdomain/zero/1.0/

Variants
--------

Several kind folks have made variants of Skycons:

*   [Color Skycons](https://github.com/maxdow/skycons) by Maxime Warnier
*   [Skycons for Android](https://github.com/torryharris/Skycons) by Torry Harris

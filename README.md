# any-browser-except-ie-internet-explorer
Images to depict that IE should have died long long ago and you should not be using it. Free to use.

Assuming you've put it in a folder of 'assets/img/' the following will show it for IE.
```
<body>
  <!-- Content .... -->
  
  <noscript>Please enable JavaScript to continue using this application.</noscript>

  <script>
    (function () {
      var noscript = document.getElementsByTagName('noscript');
      var parent = document.getElementsByTagName('body')[0];
      // remove
      for (var i in noscript) {
        parent.removeChild(noscript[i]);
        break;
      }

      var ua = window.navigator.userAgent;
      var msie = ua.indexOf("MSIE ");
      var isIE11 = !!window.MSInputMethodContext && !!document.documentMode;

      if (msie > 0 || isIE11) // If Internet Explorer, return version number
      {
        var h = document.createElement("H1");
        var noIeText = 'Internet Explorer is not supported. Please use Chrome/ Firefox/ Safari/ Edge.';
        var t = document.createTextNode(noIeText);
        h.appendChild(t);
        document.body.appendChild(h);


        var img = document.createElement('img');
        img.src = 'assets/img/any-browser-except-ie-small.png';
        img.alt = noIeText;
        img.title = noIeText;
        document.body.appendChild(img);
      }
    })();
  </script>

</body>
```

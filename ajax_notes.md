# Ajax Notes
-Ajax is faster, because it lets your build webpages by brining in data and using JavaScript to build the page quickly.
-There is a request and a response. (xmlhttp requests)
-Lets see if we can make this happen

## How Ajax Works
-The process of using JS to send a request to a server.
-Asynchronous requests load without waiting.
1. Create and XMLHTTP request object
2. Create a callback function
3. Open a request
4. Send the request

## A Simple AJAX Example
*Syntax for step 1(in html)*
```
<script>
  var xhr = new XMLHttpRequest();
</script>
```
*Syntax for step 2*
```
<script>
    var xhr = new XMLHttpRequest();
    xhr.onreadystatechange = function () {
      if (xhr.readyState === 4) {
        document.getElementById('ajax').innerHTML = xhr.responseText;
      }
    };
  </script>
  ```
*Syntax for step 3*
```
<script>
  var xhr = new XMLHttpRequest();
  xhr.onreadystatechange = function () {
    if (xhr.readyState === 4) {
      document.getElementById('ajax').innerHTML = xhr.responseText;
        }
      };
  xhr.open('GET', 'sidebar.html');
</script>
```

*Syntax for step 4*
```
<script>
  var xhr = new XMLHttpRequest();
  xhr.onreadystatechange = function () {
    if (xhr.readyState === 4) {
      document.getElementById('ajax').innerHTML = xhr.responseText;
        }
      };
  xhr.open('GET', 'sidebar.html');
  xhr.send();
</script>
```

## GET & POST
-

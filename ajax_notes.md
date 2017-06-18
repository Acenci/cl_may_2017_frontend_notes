# Ajax Notes
-Ajax is faster, because it lets your build webpages by brining in data and using JavaScript to build the page quickly.
-There is a request and a response. (xmlhttp requests)
-Lets see.

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
-Use GET when you want info from a server(sends in URL)
-Use POST to send to a server (sends data seperate from a URL)
-Query string name/property=value
-can use multiple query strings using &
-Must convert in some cases when using GET
  & = %26
  Space = +
  + = %
-Post has its own special coding

## AJAX Response Formats
-Xml(extensible markup language)
  *Syntax Ex.*  
  ```
  <contacts>
    <contact>
      <name>Andrew</name>
      <phone>555-555-5555</phone>
    </contact>
    <contact>
      <name>John</name>
      <phone>551-555-5555</phone>
    </contact>
  </contacts>
  ```
-You can create you own XML tags.

## Ajax Callbacks
-This is the programing you want to run when what you have submitted returns.
-`readyState` holds a number from 0-4 each representing step in the AJAX process.
-Add a status property `&& xhr.status === 200`, 200 equals ok, 404 is bad, and 500 is something wrong with the server.

## JSON
-JavaScript Object Notation
-Passes information around, using array and object notation.
*JSON Syntax*
```
[
  {
    "name" : "Jim",
    "phone" : "505-555-5555"
  },
  {
    "name" : "Tom",
    "phone" : "502-555-5555"
  }
]
```
-Requires double quotes

## Parsing JSON Data
-JSON has to be converted to JavaScript, this is done by what is called parsing.
-`var.responseText` is how to get your response from the server.
*Syntax to Parse*
```
var variableName = new XMLHttpRequest();
variableName.onreadystatechange = function () {
  if(variableName.readyState === 4) {
    var employees = *JSON.parse*(variableName.responseText);
  }
};
variableName.open('GET', 'data/emplyees.json');
variableName.send();
```

## Processing JSON
1. Create a new HTML list item
2. Check the "status" property
3. Get the value for the "name" property; insert it inside an <li> tag.
4. Close the <li> tag

## AJAX & jQuery
-Can use `$.` method
*jQuery .get Syntax*
```
$.get(url, data, callback);
```

## AJAX & jQuery ($.post) Method
*Syntax*
```
$.post(url, data, callback)
```
## jQuery AJAX method
-`$.ajax`
-You can do anything AJAX can do with `$.ajax`

## Handling Errors
*.fail Syntax*
```
.fail(function (jqXHR){
    jqXHR.status
  });
```

## What Is an API?
-Application Programing Interface, which allows people to access content from other servers.
-Connects your site to a third party site.

# http_framework
The  **_http**  is the object that you will work with.

I'm create two version: 
* XHR version
  * use the XMLHttpRequest 

*FETCH version
  * use the fetch to request data

___

> xhr - version

This version use the object XMLHttpRequest, you will always work with the **_http** object.

Examples ->
* GET
```javascript
/* Always start with _http.menu({options}); */

_http.menu({ // you need create an object on the fly
  type: 'GET', // GET option
  url: 'test.txt' // URL option
 }, function (err, data) { // the callback function
            if(err){
               /* do something */
            } else {
              console.log(data);
            }
          }               
);

```
* POST
```javascript
/* Always start with _http.menu({options}); */
_http.menu({
  type: 'POST', // POST option
  url: 'your url here', // URL option
  data:{
          name: "Cielo",
          code: "CIEL3",
          description: "Cielo is the first company ...",
          balance: {
                      y2018: {
                                revenue: 201541,
                                profit: 25154,
                                margin: "23%"
                             }
                   }
       }
}, (err, post) => err ? console.log(err): console.log(post) //callback using the ternary operator
);
```

* PUT
```javascript
/* Always start with _http.menu({options}); */
_http.menu({
  type: 'PUT', // PUT option
  url: 'your url here', // URL option
  data:{
    title: "Custom post",
    body: "this is a custom post!"
    }
}, callback); // whatever function callback that you wanna use

```
* DELETE
```javascript
/* Always start with _http.menu({options}); */
_http.menu({
  type: 'DELETE', // DELETE option
  url:  'your url here', // URL option
}, callback); // whatever function callback that you wanna use to verify if the post was deleted

```





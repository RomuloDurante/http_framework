# http_framework :computer:

The  **_http**  is the object that you will work with.

I'm create two version: 
* XHR version
  * use the function constructor XMLHttpRequest 

* FETCH version
  * use the global method fetch() and promises
___
## I am a student, so feel free to correct my mistakes.. :thumbsup:
___

> xhr - version

This version use  XMLHttpRequest, you will always work with the **_http** object.

Examples ->
* GET
```javascript
/* Always start with _http.menu({options}); */

_http.menu({ // you need create an object on the fly
  type: 'GET', // GET option
  url: 'test.txt' // url option
 }, function (err, data) { // the callback function
            if(err){
               /* do something */
            } else {
              console.log(data); /* do something with your data here */
            }
          }               
);

```
* POST
```javascript
/* Always start with _http.menu({options}); */
_http.menu({
  type: 'POST', // POST option
  url: 'your url here', // url option
  data:{ // data that you send to database
          name: "Cielo", // this is an example, it's can be whatever data you want (variables, objects, etc)
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
},(err, post) => err ? console.log(err): console.log(post)//callback using the arrow function and ternary operator
);
```

* PUT
```javascript
/* Always start with _http.menu({options}); */
_http.menu({
  type: 'PUT', // PUT option
  url: 'your url here', // url option
  data:{ // data that you replace in database
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
___
> fetch - version

This version use global method fetch() and promises, you will always work with the **_http** object.

Examples ->

* GET
```javascript
/* Always start with _http.menu({options}); */
_http.get('your url here') // get method
.then(function(data) {
  console.log(data) // do something whith your data here
} )
.catch(function(err) {
  console.log(data) // do something 
});
```

* POST
```javascript
/* Always start with _http.menu({options}); */
_http.post({ // Create an object on the fly to options
  url: 'url here', // url option
  data: { // data option
          title: 'this is a test', //the data you will send
          body: 'this is body test !....'
  }
}).then(data => console.log(data)) // you may use the arrow functions
  .catch(err => console.log(err));
```

* PUT
```javascript
/* Always start with _http.menu({options}); */
_http.put({  // Create an object on the fly to options
  url:  'url here', // url option
  data: {
          title: 'this is a test', // the data you will replace
          body: 'this is body test !....'
     }
}).then(data => console.log(data)) // you may use the arrow functions
  .catch(err => console.log(err));

```


* DELETE
```javascript
/* Always start with _http.menu({options}); */
_http.delete({ // Create an object on the fly to options
  url: 'https://jsonplaceholder.typicode.com/posts/2',
}).then(data => console.log(data)) 
  .catch(err => console.log(err));

```






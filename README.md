# http_framework
//*****//

Simple framework to work with requests

examples with xhr ->
_http.menu({
  type: 'GET',
  url: 'test.txt'
 }, function (err, post) {
                          _http.getTxt(post);
                          document.body.innerHTML ="<h2>" + _http.data + '</h2>';
                          console.log(_http.data);
                          }
);
/************************************/
example with fetch ->
_http.get('https://jsonplaceholder.typicode.com/posts')
.then(data => console.log(data))
.catch(err => console.log(err));


_http.post({
  url: 'https://jsonplaceholder.typicode.com/posts',
  data: {
          title: 'this is a test',
          body: 'this is body test !....'
  }
}).then(data => console.log(data))
  .catch(err => console.log(err));

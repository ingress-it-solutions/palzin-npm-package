
# Palzin API

## Install
> npm install palzin-npm-package

## Using
> pz.api(method, [options], [callback]);
>
> Use request options. More details [here](https://www.npmjs.com/package/request#requestoptions-callback)


```javascript
const pz = require('PalzinJS')();

pz.init({
  username: 'member@ingressit.com',
  password: 'Easy to remember, hard to guess',
  client_name: 'My Awesome NodeJS App',
  client_vendor: 'Ingress IT Solutions',
  host: 'http://projects.ingressit.com/'
}, (err, response) => {
  let options = {
    json: true,
    method: 'POST',
    headers: [/* You can add custom headers */],
    body: {
      name: 'Task #1',
      labels: ['New','Deferred']
    }
  };

  pz.api('/projects/1/tasks', options, (err, response) => {
    console.log(response);
  });
});
```

# jsConsole-discordTokenGrabber

Getting Discord token with javascript console.

Who knows what you are going to do with this code.

## Usage

* Open Discord in any supported browser(See below). And then paste the code into js console.

### Readable version

```js
function getToken() {
  // start a new tab/window under the same url
  let window = window.open();
  
  // check if the popup/new window opened successfully
  if(window || !window.document) {
    return console.error('Unable to get token: popup blocked!');
  }
  
  // fooling localStorage trick
  window.dispatchEvent(new Event('beforeunload'));
  
  // log token
  console.log(window.localStorage.token);
  
  // clean up
  window.close();
};

getToken();
```

### One-liner pasta for javascript console

```js
(function(){let w=window.open();if(!w||!w.document)return console.error('Unable to get token: popup blocked!');window.dispatchEvent(new Event('beforeunload'));console.log(w.localStorage.token);w.close()}());
```

### Tested browsers:

| Browsers       | Supported    |
| :------------- | -----------: |
| Chrome         | :heavy_check_mark:   | 
| Safari         | :x: |

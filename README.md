# jsConsole-discordTokenGrabber

Getting Discord token with JavaScript console.

Who knows what you are going to do with this code.

## Usage

* Open [Discord](https://discordapp.com/login) in any supported browsers(See below). And then paste the code into the JavaScript console(AKA inspect element console) after logging in.
* Note: This code won't work in discord desktop app.

### Readable version

```js
function getToken() {
  // start a new tab/window under the same url
  let win = window.open();
  
  // check if the popup/new window opened successfully
  if(!win || !window.document) {
    return console.error('Unable to get token: popup blocked!');
  }
  
  // fooling localStorage trick
  window.dispatchEvent(new Event('beforeunload'));
  
  // log token
  console.log(win.localStorage.token);
  
  // clean up
  win.close();
};

getToken();
```

### One-liner pasta for javascript console

```js
(function(){let w=window.open();if(!w||!w.document)return console.error('Unable to get token: popup blocked!');window.dispatchEvent(new Event('beforeunload'));console.log(w.localStorage.token);w.close()}());
```

### Tested browsers:

- :heavy_check_mark: Works with default browser settings
- :x: Doesn't work with default browser settings
- :grey_question: Will ask user to enable/allow popup window

| Browsers       | Supported            |
| :------------- | :------------------: |
| Chrome         | :heavy_check_mark:   |
| Safari         | :x:                  |
| Firefox        | :grey_question:      |
| Edge           | :heavy_check_mark:   |

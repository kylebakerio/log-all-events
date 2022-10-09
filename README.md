# a-console
A better, canvas-based console for A-Frame. Currently in 'alpha', but should already be the best thing out there. Prints to a virtual 1920x1080 screen vertically oriented. Prints stack traces for errors. Handles line breaks and auto-scrolls on new input. Stringifies and pretty-prints objects that are console-logged. 

<a href='https://ko-fi.com/kylev' target='_blank'><img height='35' style='border:0px;height:46px;' src='https://az743702.vo.msecnd.net/cdn/kofi3.png?v=0' border='0' alt='Buy Me a Coffee at ko-fi.com' /><a/>

## demo
https://canvas-log.glitch.me/

## how-to
Literally just add this line to your scene:
```html
<a-console position="0 1.5 -2"></a-console>
```

by default it will intercept console.log/warn/error, and print stack traces on error. you can also manually print to the console with the `logToCanvas()` and `writeToCanvas()` methods. (They do _not_ currently run commands, just allow you to print text.)

## options
**I always advise that you check the schema for up-to-date options.**
```js
    // I recommend not touching these:
    fontSize: {default: 18, type: 'number'},
    fontFamily: {default: 'monospace', type: 'string'},
    canvasWidth: {default: 1080, type: 'number'},
    canvasHeight: {default: 1920, type: 'number'},
    // but you can touch these:
    backgroundColor: {default: 'black', type: 'color'},
    textColor: {default: 'green', type: 'color'},
    captureConsole: {default: ['log','warn','error'], type: 'array'},
    capturedConsoleColors: {default: [null,'yellow','red'], type: 'array'},
    printStackTraceFor: {default: ['error'], type:'array'},
    captureConsoleActive: {default: true, type:'bool'},
```

## roadmap
  - reflow text for custom terminal sizes 
  - ability to manually scroll, not just auto-scroll
  - inclusive/exclusive filter
  - allow JSON stringify custom settings
  - make stack traces toggle/revealable
  - keyboard for console input
  - `eval()` to run code on the fly from inside VR
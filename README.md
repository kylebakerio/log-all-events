![jsDelivr hits (GitHub)](https://img.shields.io/jsdelivr/gh/hm/kylebakerio/log-all-events)

# log-all-events

## features
- includes synthetic and native events
- some settings to modify verbosity
- combine with [a-console](https://github.com/kylebakerio/a-console) to see these events in VR, as per demo

```html
<head>
    <!-- add aframe first, then add this component -->
    <script src="https://cdn.jsdelivr.net/gh/kylebakerio/log-all-events@0.1.0/log-all-events.js"></script>
</head>
```

```html
<a-scene>
   <a-entity log-all-events></a-entity
</a-scene>
```

options:
```js
  schema: {
    skip: {default: [], type: 'array'},
    debug: {default: false, type:'bool'},
    includeFullEventObject: {default: false, type:'bool'},
    includeEvtDetail: {default: true, type:'bool'},
    consoleMethod: {default:'log', type:'string'},
    nativeEvents: {default:true, type:'bool'},
    syntheticEvents: {default:true, type:'bool'},
    timestamp: {default:true, type:'bool'},
  },
```  

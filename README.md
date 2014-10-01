GPSDetector
===========

Features
--------

- Check if your device has GPS enabled or not.
- Tested (and working) on Android 4.4 KitKat (Nexus 5)
- This fork is only tested with cordova 3.6.3-0.2.13, but I'm sure it's fine!


Installation
------------
```
cordova plugin add https://github.com/chevett/GPSDetector
```

Usage
-----

```js
document.addEventListener("deviceready", onDeviceReady, false);

function onDeviceReady() {

	if (!Window.GPSDetector) return;

	Window.GPSDetector(onGPSSuccess, onGPSError);
	
	function onGPSSuccess(enabled) {
		alert(enabled ? 'GPS is ON' : 'GPS is OFF');
	}
	
	function onGPSError(e) {
		alert('GPSDetector is busted: ' + e);
	}
}
```

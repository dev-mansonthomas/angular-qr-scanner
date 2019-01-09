angular-qr-scanner-updated
==================

Based on angular-qr-scanner which is no longer maintained.

This library allow you to use the webcam to decode a QRCode.

Angular directive for a QR Scanner. It is the angular version of [html5-qrcode](https://github.com/dwa012/html5-qrcode) and uses [jsqrcode](https://github.com/LazarSoft/jsqrcode).

Check out the [live demo](http://sembrestels.github.io/angular-qr-scanner/), it may still be working.

### Important : HTTPS required 
To be able to use the webcam in a browser, your website must be on https, otherwise browser won't give access to the webcam.

For dev mode, localhost allow to use the webcam without https.


### Usage

```html
<qr-scanner ng-success="onSuccess(data)" width="400" height="300"></qr>
```

### Install

```sh
$ bower install angular-qr-scanner-updated
```

### Example

```html
<html ng-app="App">
<body ng-controller="qrCrtl">
<qr-scanner width="400" height="300" ng-success="onSuccess(data)" ng-error="onError(error)" />

<script src="http://ajax.googleapis.com/ajax/libs/angularjs/1.6.4/angular.js"></script>
<script src="bower_components/angular-qr-scanner/qr-scanner-u.js"></script>
<script src="bower_components/angular-qr-scanner/src/jsqrcode-combined.min.js"></script>
<script>

var App = angular.module('App', ['qrScannerU']);

App.controller('qrCrtl', ['$scope', function($scope) {
    $scope.onSuccess = function(data) {
        console.log(data);
    };
    $scope.onError = function(error) {
        console.log(error);
    };
    $scope.onVideoError = function(error) {
        console.log(error);
    };
}]);

</script>
</body>
</html>
```

### License
The MIT License

Copyright (c) 2013-2015 Sembrestels

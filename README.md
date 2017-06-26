# things-ajax
## 1. Explanation
### The component exposes xhr request function.

The `things-ajax` element exposes xhr request functionality.
```html
    <things-ajax
        auto
        url="http://gdata.youtube.com/feeds/api/videos/"
        params='{"alt":"json", "q":"chrome"}'
        handle-as="json"
        on-response="handleResponse"
        debounce-duration="300"></things-ajax>
```
With `auto` set to `true`, the element performs a request whenever its `url`, `params` or `body` properties are changed.</br>
Automatically generated requests will be debounced in the case that multiple attributes are changed
sequentially.
* _Note: The `params` attribute must be double quoted JSON. You can trigger a request explicitly by calling `generateRequest` on the element._
****

## 2. Development
### 2.1 Install Polymer-CLI

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `polymer serve` to serve your application locally.

### 2.2 Run Application

```
$ polymer serve
```

### 2.3 Build Application

```
$ polymer build
```

You can launch the server from `build/bundled` or `build/unbundled` with the following command:

```
$ polymer serve build/bundled
```

### 2.4 Run Tests

```
$ polymer test
```

The test has been set up as described in [web-component-tester](https://github.com/Polymer/web-component-tester).
You can run the test with the following command.
```
$ polymer test
```

# things-ajax
## 1. 설명
### 해당 컴포넌트는 xhr request 기능을 노출한다.

```html
    <things-ajax
        auto
        url="http://gdata.youtube.com/feeds/api/videos/"
        params='{"alt":"json", "q":"chrome"}'
        handle-as="json"
        on-response="handleResponse"
        debounce-duration="300"></things-ajax>
```
만약 'auto'가 'true'로 설정되면, 이 element는 'url', 'params', 'body' 등이 변경될 때마다 request를 실행한다.</br>
여러 속성들이 순차적으로 변경되는 경우, 자동 생성된 request들은 debounce된다.
* _Note: `params` 속성은 큰 따옴표("")로 묶은 JSON 구조로 되어 있어야 한다. element에서 `generateRequest`를 호출하여 명시적으로 request를 발생시킬 수 있다._
****

## 2. 개발
### 2.1 Polymer-CLI 설치

먼저 [Polymer CLI](https://www.npmjs.com/package/polymer-cli)가 설치되어 있는지 확인한다. 다음, `polymer serve`를 실행하여 로컬에서 응용 프로그램을 제공한다.

### 2.2 Application 실행

```
$ polymer serve
```

### 2.3 Application 빌드

```
$ polymer build
```

아래 명령어로 `build/bundled`나 `build/unbundled`에서 서버를 띄울 수 있다.

```
$ polymer serve build/bundled
```

### 2.4 Test 실행

```
$ polymer test
```

[web-component-tester](https://github.com/Polymer/web-component-tester)에서 설명한 대로, 테스트 설정은 이미 완료되어 있다.
아래 명령어로 테스트를 실행할 수 있다.
```
$ polymer test
```

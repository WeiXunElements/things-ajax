# things-ajax
## 1.설명
### 해당 컴포넌트는 xhr request를 하는 기능
### ko-kr

```html
    <things-ajax
        auto
        url="http://gdata.youtube.com/feeds/api/videos/"
        params='{"alt":"json", "q":"chrome"}'
        handle-as="json"
        on-response="handleResponse"
        debounce-duration="300"></things-ajax>
```
'auto'가 'true'로 세팅되면, 이 element는 'url', 'params', 'body'등이 변하면 request을 한다.</br>
자동적으로 생성된 요청들은 다수의 속성들이 순차적으로 변화되어지는 경우에 request가 여러번 순차적으로 발생이 된다.

  * _Note: 'params'속성은 " "로 된 JSON을 해야만한다. element에서 'generateRequest'를 호출함으로써 한 요청을 발생 시킬 수 있다._

## 2. 개발
### 2.1 Polymer-CLI 설치

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `polymer serve` to serve your application locally.

### 2.2 Application 수행

```
$ polymer serve
```

### 2.3 Application 빌드

```
$ polymer build
```

아래 명령어로 ` build/bundled`나 ` build/unbundled`에서 서버를 띄울수 있다.

```
$ polymer serve build/bundled
```

### 2.3 Running Tests

```
$ polymer test
```

테스트는 [web-component-tester](https://github.com/Polymer/web-component-tester)에서 설명한데로 설정완료됨.
아래 명령어로 테스트를 수행할 수 있다.
```
$ polymer test
```

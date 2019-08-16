# Node.js의 기본모듈
Node.js의 기본적인 모듈들이다.

## Global Object
1. console 객체: 콘솔에 특정 값 출력 시 사용
```javascript
console.log('name:%s','oh jeong weon');
```

* <code>%s</code> : 문자열
* <code>%d</code> : 숫자(정수 또는 실수형)
* <code>%j</code> : JSON 형태의 문자열
* <code>%</code> : %문자 하나

<br>

2. export 객체: 특정한 모듈에 속성이나 메소드를 정의할 때 사용. <br>
Node.js도 결국 여러 모듈을 정의하고 해당 모듈을 통해 메소드와 속성을 제공해준다.
```javascript
exports.title = "calculation module";
exports.add = function(num1, num2){
  return num1 + num2;
}
```
위 코드는 덧셈을 수행하는 모듈파일 작성 예시이다.

<br>

3. process 객체
process 객체 자체에서도 다양한 이벤트 종류를 제공하고, 발생한 각 이벤트를 처리해주어야 한다.

* <code>exit</code>: 프로그램이 종료될 때 발생되는 이벤트
* <code>uncaughtException</code>: 프로그램에서 예외가 발생했을 때 발생되는 이벤트

<br>

## Path 모듈
Path모듈은 파일의 경로들을 변경해주는 기능들을 정의하고 있다. 지원되는 대부분의 메소드들은 문자열 변형만을 지원한다. 
* <code>path.normalize(p)</code>: 상대경로를 나타내는 '.'과 '..'를 인식하여 문자열의 정규경로를 반환해준다.
* <code>path.join([path1],[path2],[...]): 파라미터로 지정된 경로들을 하나로 합쳐주는 기능을 하는 메소드다.
* <code>path.resolve([from...], to)</code>: from에 지정된 경로로부터 to 경로까지 하나씩 cd명령으로 경로를 이동하면서 절대경로를 반환한다.

<br>

## os 모듈
os모듈은 운영체제와 관련된 여러가지 특성 값들과 운영체제의 상태를 얻어올 수 있는 모듈이다.


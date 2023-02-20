# Dart

```
https://dartpad.dev/
```

## main함수

main함수는 모든 Dart 프로그램의 Entry point

main 함수에서 쓴 코드가 호출 (만약 main이 없다면 실행이 되지 않음)

dart는 자동으로 **세미콜론**을 붙여주지 않기 때문에 직접 붙여야 함

일부러 세미콜론을 안 쓸 때가 있기 때문

```
void main(){
print("hello world");
}
```

## 변수 선언

```
void main() {
var name = "pizza"; // 방법 1
String name = "chicken"; // 방법 2
name = "chicken ";
}
```

function이나 method 내부에 지역변수를 선언할 때는 var

class에서 변수나 property를 선언할 때는 타입을 지정

### Dynamic 타입

여러가지 타입을 가질 수 있는 변수에 쓰임 (변수의 타입을 알 수 없을 때 주로 사용)

변수를 선언할 때 dynamic을 쓰거나 값을 지정하지 않으면 dynamic

```
void main(){
dynamic name;
var name2;
}
```

### Null Safety

개발자가 null 값을 참조할 수 없도록 하는 것

String? name 은 String 또는 null

기본적으로 모든 변수는 non-nullable(null이 될 수 없음)

```
void main() {
String? name = "hello";
name = null;
}
```

### final 변수

final변수는 수정할 수 없음 ( js의 const와 비슷 )

```
void main() {
final name = "pizza";
name = "ham"; // 수정 불가

final String username = "tony";
name = "steve"; // 수정 불가
}
```

### late 변수

데이터 없이 먼저 변수를 생성하고 나중에 데이터를 넣을 때

flutter로 data fecthing을 할 때 유용

late 변수를 만들고, API에 요청을 보낸 뒤

API에서 값을 보내주면 그 응답값을 late변수에 넣어 사용

```
void main() {
late final String name;

print(name); // name 변수에 접근 불가
}
```

### const 변수

dart에서 const는 compile-time constant ( js에서의 const와 다름 )

_값이 API로부터 오거나 사용자가 화면에서 입력해야 하는 값이라면_ => final이나 var

**const** : 컴파일 시점에 바뀌지 않는 값 (상수)

**final** : 컴파일 시점에 바뀌는 값 (API에서 받아온 값, 사용자 입력값)

```
void main() {
const name = "tony";
final username = fetchAPI();
}
```

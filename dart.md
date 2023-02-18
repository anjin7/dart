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

final변수는 수정할 수 없음 ( 자바스크립트의 const와 비슷 )

```
void main() {
final name = "pizza";
name = "ham"; // 수정 불가

final String username = "tom";
name = "tom2"; // 수정 불가
}
```

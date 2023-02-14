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

## 변수를 만드는 2가지 방법

```
void main() {
var name = "pizza"; // 방법 1
String name = "chicken"; // 방법 2
name = "chicken ";
}
```

function이나 method 내부에 지역변수를 선언할 때는 var

class에서 변수나 property를 선언할 때는 타입을 지정

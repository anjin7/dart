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

## Data type

거의 대부분의 타입들이 객체로 이루어져 있음 (함수도 객체) => `dart = 객체지향 언어`

```
void main() {
String name = "tony";
bool isPlay = true;     // boolean
int age = 10;           // integer
double money = 52.55;
num x = 12;             // integer or double
num y = 1.2;
}
```

### List

```
void main() {
List<int> numbers = [1, 2, 3];
var number2 = [4, 5, 6];
}
```

**collection if** 와 **collection for**를 지원

```
void main(){
var giveMeSix = true;
int case1 = [
1,
2,
3,
4,
5,
if(giveMeSix) 6,
];

if(giveMeSix){
case1.add(6);
}
}
```

### 변수 삽입

1. 단순 삽입은 따옴표 내부에 $변수명
2. 변수를 계산하여 삽입하는 법은 ${계산식}

\* $ 그대로 표시는 escape문자 \\$

\* String 내부에 따옴표 사용은 \\' 혹은 \\"를 사용하거나 다른 따옴표로 String 열고 닫기

### Collection For

조건문(if) 및 반복(for)을 사용하여 컬렉션을 구축하는 데 사용할 수 있는 collection if / collection for

### Maps

key와 value를 연결하는 Object

```
var food = Map();
food['korean'] = 'kimbap';
food['japanese'] = 'takoyaki';

//
// var food = {
//   'korean' : 'kimbap',
//   'japanese' : 'takoyaki'
// };

```

### Sets

Set에 속한 모든 아이템들이 유니크 할 때 사용

## Function

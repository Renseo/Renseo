# Java 개요
## 프로그래밍 언어란?
Spring을 배우고자 하는 사람이 다루게 될 언어: Java
- 컴퓨터는 어떻게 Java를 이해하는 걸까?  

일반적으로 대화를 나눌때  

• 대화의 문맥이 존재  
• 서로 상호 합의된 상식  
• 상대방에 대한 약간의 정보  

대화를 쉽게 풀어가기 위해 사용하는 것들  
___
### 기계어와 어셈블리어
컴퓨터 = 전자제품 ⇒ 전기 신호의 유무를 기준으로 작동  

신호가 있다? ⇒ 1  
신호가 없다? ⇒ 0  

동시에 여러 신호를 받자

01101001

이 신호 조합에 따라 다르게 작동하게 만들어 보자 -> 기계어  

기계어 : CPU가 입력받아 해석할 수 있는, 0과 1로 이루어진 명령어 (또는 프로그래밍 언어...?)  

어셈블리어(Low Level Programming Language) : 기계어와 대응되는, 인간이 읽을 수 있는 형태의 프로그래밍 언어  
___
### High Level Language

High Level Language 자체를 CPU가 직접 실행할 수는 없다!
- Java를 비롯한 High Level Language로 작성된 코드는 어느 시점에 다시 기계어로 변환되어야 한다.

- 변환의 시점은 언어(의 구현체)마다 다르다.

실행 전에 기계어로 미리 번역됨 ⇒ 컴파일 언어  
실행 하면 그때그때 기계어로 번역됨 ⇒ 스크립트 언어
___
## Java
### Java와 JVM

Java 언어를 ‘컴파일’하면 무엇이 나올까?
- Java Bytecode 라는게 나온다.
- Java Bytecode는 쉽게 생각하면 JVM을 위한 어셈블리어.
- 그리고 JVM은 Java Bytecode를 CPU가 이해할 수 있는 기계어로 번역한다.
___
### JDK와 JRE
JVM이 컴퓨터와 소통을 해주고, JVM은 Java Bytecode를 필요로 한다.
- 그럼 우리가 작성한 Java 코드는 어떻게 Java Bytecode로 변환할까?
- Java Development Kit를 활용하자!

Java Development Kit
- Java를 개발하기 위한 도구 모음집
- Java 언어를 Java Bytecode로 변환하는 컴파일러(javac)
- Java Bytecode를 실행해보기 위한 JVM 등

그럼 Java로 만들어진 프로그램을 사용하기 위해선 JDK가 필요할까?
- 만들어진 프로그램을 쓰기만 하는데 개발도구 다 갖출 필요는 없다.
- 프로그램 실행을 위한 것들만 따로 모으자 ⇒ JRE
- JRE: JVM과 JVM이 사용할 기타 라이브러리를 포함한, Java로 작성된 프로그램의
실행 환경
___
### JDK 설치하기
OpenJDK든 GraalVM이든...
- 목표는 CLI 환경 (cmd, terminal, 기타등등...)에서 java와 javac 명령어가 잘 작동
하도록 하는 것!
- OpenJDK (19이상) - https://jdk.java.net/
- OpenJDK Archive (18이하 버전) - https://jdk.java.net/archive/
- GraalVM - https://www.graalvm.org/downloads/
___
### 코드 작성 도구들
코드를 작성하는건 어려운 일이다
- 익숙하지 않은 영어를 사용하는 경우가 많고
- 일상 대화와 달리 문법적 오류를 허락하지 않으며
- 쉼표나 세미콜론 같은 것도 잊어선 안된다.

Java 프로젝트를 진행하려면 어떤 도움을 받으면 좋을까?
- 문법과 맞춤법 등을 확인해 준다면?
- 완성된 코드를 좀더 쉽게 실행해 준다면?
- Code Editor와 IDE  

Code Editor
- 코드를 작성하는데 도움을 주는 도구 (문법 검사, 글자 색 조정 등)
- 비교적 가볍고 빠르며 인터페이스가 단순하다.

IDE (Integrated Development Environment)
- 단순 코드 문법 검사를 넘어, 프로젝트의 시작부터 완성까지 도움을 주는 도구를
갖춘 통합 개발 환경
- 상대적으로 무겁지만, 좀더 정교한 기능을 갖춘 경우가 많다.

하지만 결국 IDE는 도우미이다.
- 프로젝트를 진행하는데 도움을 주는 역할이다.
- IDE를 잘 활용하기 위해서는 결국 자신이 사용하고자 하는 언어 / 프레임워크가
어떤 원리로 작동하는지 알 필요가 있다.
___
## Hello World!
`IntelliJ IDEA` 실행 - `New project`  
`Name: hello-hava`  
`JDK: 17 GraaIVM version 17.0.7`

왼쪽 탭에서 `src`폴더에 `Class` 생성

```java
public class HelloJava {
    public static void main(String[] args) {
        System.out.println("Hello Java!!!");
    }
}
```
단축키 `Shify + alt + F10` 으로 실행  
실행결과
```
Hello Java!!!
```
___
### 주석
코드에 대한 설명을 위해 주석을 달 수 있다.
- `//`: 한줄 주석, 이후의 코드 무시
- `/* */`: 블록 주석, 시작부터 끝까지의 코드 무시
___
### 간단한 입력 - Scanner
아래의 코드는 사용자한테 한줄의 코드를 입력받고, 다시 출력한다.

```java
// 지금은 의미에 대해 깊이 생각하지 맙시다.
Scanner scanner = new Scanner(System.in);
System.out.println(scanner.nextLine());
```
실행결과
```java
Hello Java!!!
만나서 반갑습니다!!! // 키보드로 입력한 내용 + Enter
만나서 반갑습니다!!! // 출력된 결과
```

## 변수 & 자료형

### 변수
변수 - 데이터를 담는 상자와 같은 역할
```java
public class HelloJava {
    putblic static void main(String[] args) {
        int a = 100;
        System.out.println(a);
        String b = "Hello Variables!";
        System.out.println(b);
    }
}
```
- 할당 연산자(=)를 이용해 값을 저장
(할당)할 수 있다.
- <자료형> <이름> = <값>
- 변수를 만드는 걸 선언(declare)한다
고 부른다.
- 변수의 값은 다시 할당할 수 있다.

선언과 할당은 반드시 한번에 이뤄질 필요는 없다.
```java
int date;
// 어떤 작업 이후
date = 100;
```
한 줄에 여러 변수를 동시에 선언할 수도 있다.
```
int month = 11, day = 20;
```

### 변수 이름 짓기
문법적인 관점
1. 숫자로 시작할 수 없다. (1st, 2nd 등)
2. _ 와 $ 외의 특수문자를 사용할 수 없다. (maxInt# 등)
3. int, class, return 등의 예약어(Java 내부적으로 사용하는 단어, Keyword)를 사용할 수 없다.

변수의 이름과 같이 개발자가 정할 수 있는 이름을 식별자(identifier)라고 부름  

Naming Convention
- 서로 다른 개발자가 이름을 보았을 때 그것이 무엇인지(변수인지 아니면 다른 무엇인지) 알아볼 수 있도록 상호 합의된 규칙
- Java에서 변수 이름을 정할 때는 일반적으로 `camelCase`로 짓는다.
- 기본적으로 소문자 활용
- 여러 단어를 변수 이름에 쓰고 싶다면, 단어가 바뀌는 시점에 대문자를 활용

```java
int 1stVar = 10;     // 문법적으로 올바르지 않기 떄문에 실행되지 않습니다.  
int second_var = 23; // 문법적으로는 오류가 없지만, Naming Convention에 어긋납니다.
int thirdVar = 42;   // Java에서 변수 이름을 짓는 옳은 방법입니다.
```

### 자료형
데이터의 종류
- 어떤 변수를 선언하면서, 해당 변수가 어떤 데이터를 저장할 수 있는지를 정의
- 어떤 자료형을 가진 변수에, 다른 자료형의 데이터를 할당하려고 하면 오류가 발생

```java
int intNumber = 10;
double realNumber = 365.25;
char character = 'a';
boolean trueOrFalse = true;
String string = "this is string";
```

### 정수 자료형
주로 `int`, `long`이 활용된다.  
자료형|최소|최대|
:-|-|-
`int`|-2147483648|2147483647
`ling`|-9223372036854775808|9223372036854775807
`short`|-32768|32767
`byte`|-128|127

```java
int integer = 10;
long bigInteger - 1000000000L;
short smallInteger = 10000;
byte reallySmallInteger = 127;
```

### 실수 자료형
`float`, `double`이 있으며, 기본적으로 소숫점을 사용해 숫자를 표현하면 `double`이 된다.
자료형|최소|최대|유효자리수
:-|-|-|-:
`float`|-3.4*10^38|3.4*10^38|7
`double`|-1.7*10^308|1.7*10^308|16
```java
float floatPoint = 2.718281F;
double doublePoint = 3.14159265359;
```
유효자리를 벗어나면 나머지는 반올림된다.
```java
double longPi = 3.14159265358979323846;
```

### 불린(`boolean`) 자료형
참 또는 거짓을 표현하기 위한 자료형. 데이터 자체는 `true` 또는 `false`로 나타낸다.  
```java
boolean success = false;
boolean willSuccess = true;
```
상태를 표현하기 위한 용도로 많이 활용되며, 제어문과 많이 사용된다.

### 문자(`char`) 자료형
단일 문자를 표현하기 위한 자료형
```java
char alphabet = 'a';
char charRepInt = '1';
```
작은 따옴표를 사용한다.

### 문자열(`String`) 자료형
여러 글자를 합쳐 단어, 문장 등을 표현하기 위한 문자(`char`)들의 나열
```java
String word = "Hello";
String sentence = "this is a String variable.";
```
큰 따옴표를 사용

## 데이터 입력받기

### `Scanner`로 다양한 데이터 받기
```java
//지금은 의미에 대해 깊이 생각하지 맙시다.
Scanner scnner = new Scanner(System.in);
System.out.println(scanner.nextLine());
```

```java
byte scanByte = scanner.nextByte();
short scanShort = scanner.nextShort();
int scannedInt = scanner.nextInt();
long scanndeLong = scanner.nextLong();
System.out.println(scannedByte);
System.out.println(scannedShort);
System.out.println(scannedInt);
System.out.println(scanndeLong);
```
- 기본적으로 받고자 하는 자료형의 이름이 담긴 메서드를 사용한다.
- 메서드는 추후 더 자세히 다룬다.

```java
float scanFloat = scanner.nextFloat();
double scanDouble = scanner.nextDouble();
```
`float` 데이터를 받는다고 굳이 입력에 F를 넣어주지 않는다. 오히려 오류가 발생한다.

```java
boolean scanBool = scanner.nextBoolean();
```
`true`, `false`를 대소문자 구분없이 넣어줄 수 있다.

```java
System.out.println("scnner.nextLine");
```
엔터 입력까지 한줄의 문자열을 입력받는다.

### Scanner 사용시 주의점
```java
byte scanByte = scanner.nextByte();
short scanShort = scanner.nextShort();
int scannedInt = scanner.nextInt();
long scanndeLong = scanner.nextLong();
```
위와 같은 코드에서, 1 1 1 1 처럼 공백으로 구분된 정수 넷이 입력되면?
- 네 줄의 코드가 동시에 동작한다.
- `Scanner`는 한 줄의 입력에 대해서 동작하는게 아니라, 입력된 모든 내용에서 일치하는 데이터를
찾는다.

## 문자열 응용

### Escape Sequence

문자열 내부에 특수한 문자를 표현하고 싶다면?
- 문자열은 `“`를 쓰는데, 쓰고 싶은 데이터도 `“`라면?
- String 변수안에 다음 줄을 쓰고 싶다면?
- 탭 같이 동작하는 들여쓰기?

`Escape Sequence` – 키보드로 입력하기 어려운 특수한 문자를 표현하기 위해 사용되는 문자 조합
- `Escape Character` – `Escape Sequence`를 만들기 시작한다는 의미의 특수문자`,` 주로 `\`가 활용됨

#### 특수문자 표현하기
```java
// 문자열 내부에 " 표현하기
System.out.println("\"");
// cahr 데이터로 ' 표현하기
System.out.println('\'');
// 문자열 내부에 \ 표현하기
System.out.println("\\");
```

Escape Sequence|결과
-|-
\n|다음 줄
\t|탭
\r|캐리지 리턴
\b|백스페이스

```java
System.out.println("개행문자: \n이 다음은 다음 줄이 표현됩니다.");
System.out.println("탭키: \t다음 탭의 위치까지 옮긴 뒤 표현됩니다.");
System.out.println("Carriage Return: \r줄의 앞으로 옮깁니다.");
System.out.println("백스페이스: \b앞의 문자를 하나 지웁니다.");
```

실행결과

```
개행문자:
 이 다음은 아래줄에 표현됩니다.
탭키:   다음 탭의 위치까지 옮긴 뒤 표현됩니다.
줄의 앞으로 옮깁니다.
백스페이스:앞의 문자를 하나 지웁니다.
```
실제 문자라기보단, 화면상의 커서를 옮기라는 명령이다.

### String Formatting
어떤 문구를 문자열로 나타낸다고 할 때, 상황에 따라 일부분만 바꿔서 여러번 표현하고 싶은 경우가 생길 수 있다.

```java
String message = "미세먼지 농도: 10 (좋음)";
```
농도와 상태 메시지(좋음)은 다른 변수에 저장해도 괜찮지 않을까?
```java
int dust = 10;
String status = "좋음";
// 미세먼지 농도: 10 (좋음)
System.out.println(String.format("미세먼지 농도: %d (%s)", dust, status));
```
Java에는 여러 방법이 있지만, 주로 `String.format()`을 많이 활용한다.
- 템플릿 역할을 하는 문자열을 넣어주고,
- 뒤에 템플릿에 사용할 값들을 넣어준다.
- 최소한 템플릿에서 필요로 하는 만큼의 값들은 넣어주어야 한다.

코드|자료형
:-|-
%s|문자열(String)
%c|문자(char)
%d|정수(int)
%f|부동소수(float, double)

포맷 코드(format specifiers)
어떤 자료형의 데이터가 표현 될지를 문자열 내부에 지정하는 방법
```java
System.out.println(String.format("미세먼지 농도: %d (%s)", dust, status));
System.out.println(String.format("초미세먼지: %d", dust));
System.out.println(String.format("오존: %.4f", 0.0229));
```

## 배열
배열 - 하나의 변수에 여러 데이터를 정리하여 저장하기 위해 사용한다.
```java
int[] scores = {85, 75, 90};
```

- 변수를 선언할 때, 자료형 뒤에 [] 를 덧붙여 선언, 그 뒤 {}를 이용해 저장할 값들을 나열한다.
- 이후 다시 가져올 때는 변수에 [] 를 이용하며, [] 안에 몇번째 값을 가져올지를 지정한다.
- 첫번째 아이템은 0이다.
```java
int[] scores = {85, 75, 90};

System.out.println(scores[0]);
System.out.println(scores[1]);
System.out.println(scores[2]);
```

- 내부의 개별 데이터를 바꿔줄 때도 [] 를 이용해 접근, = 를 이용해 할당할 수 있다.

```java
int[] scores = {85, 75, 90}
scores[1] = 80;
System.out.println(scores[0]);
System.out.println(scores[1]);
System.out.println(scores[2]);
```

- 배열에 들어갈 데이터가 정해지기 전이라면, 크기를 먼저 결정해서 할당할 수 있다.
```java
String[] names = new String[4];
names[0] = "alex";
System.out.println(names[0]);
```
- 문법 자체는 지금은 신경쓰지 말자.

- 크기를 정할 때, 그 크기도 마찬가지로 변수로 전달할 수 있다.
```java
int students = 10;
        String[] names = new String[students];
        scores = new int[students];
```
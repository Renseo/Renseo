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
Java 언어의 모토? ⇒ Write Once Run Anywhere
- 한번 작성한 코드를 어떤 컴퓨터에서든 실행할 수 있도록!
- CPU마다 받아들이는 기계어가 다른데 어떻게?

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
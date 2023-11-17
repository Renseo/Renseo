# Markdown
## Markdown 특징
1. 마크업 언어 (Markup Language)의 일종
2. 관리가 쉽다
3. 별도의 도구없이 쉽게 작성이 가능하다.
4. 다양한 플랫폼에서 사용한다.

#### 어떤 직업을 가지든 자신이 한 작업을 보여줄 수 있어야 한다.
- 마크다운은 개발자가 자신의 작업을 보여주기 위해 가장 흔히 사용하는 방법이다.

### Markup Languge
문서가 표현하는 데이터가 어떤 구조를 가지고 있는지를 명시하기 위한 언어 및 기호의 집합
대표적인 Markup Language (Markdown, HTML)

## Markdown 사용법
# 문단 제목
#문단 제목1
## 문단 제목
##문단 제목2  
### 문단 제목
###문단 제목3  
#### 문단 제목
####문단 제목4  
##### 문단 제목
#####문단 제목5  
###### 문단 제목
######문단 제목6  
___
### 문단 (Paragraphs)
문단입니다.
엔터 한번으로는 줄이 안바뀝니다.

엔터 두번이 되어야 줄이 바뀌고,
다음문단으로 인식합니다.
___

### 줄바꿈 (Line Breaks)
새로운 문단이 아닌, 문단 내부에서 엔터를 추가하고 싶다면 
공백 두개와 함께 엔터를 해주면 줄이 바뀝니다.
___

### 글 강조 (Emphasis)

#### 굵은 글씨
굵은 글씨를 표현하고 싶다면 **별을 두개** 넣어주세요. -> \*\*단어**

#### 기울인 글씨
기울인 글씨는 *별 하나*로 만들 수 있습니다. \*단어\*

#### 굵게 기울인 글씨
굵으면서 기울인 글씨는 ***별이 세개*** 필요합니다. \*\*\*단어***
___

### 인영문 (Block Quotes)
아래는 인용문을 나타냅니다.

> A quotation is the repetition of a sentence, phrase, or passage from speech or text that someone has said or written. \'> 내용'
___

### 목록 (List)

#### 순서를 가진 목록  
내용 앞 숫자를 기입하여 순서를 나눈다. 숫자의 크기 상관없이 작동한다.  

아침에 할일
1. 일어나기
2. 세수하기
3. 컴퓨터 켜기
4. 코딩


#### 순서가 없는 목록
사용할 수 있는 언어
- JAVA
- Python
- JavaScript

#### 하위 목록
목록을 작성한 후 다음 줄에서 Tap키를 입력하여 작성한다.
1. 일어나기
2. 세수하기
3. 컴퓨터 켜기
4. 코딩
    - 백준
    - 프로그래머스
___

### 코드 (Code)
문단 내부의 일부를 소스코드처럼 변경  
마크다운에서 코드를 표현하고 싶다면, `printf("Hello World!")` 라고 써봅시다. -> \`코드`  

문단 내부의 일부를 소스코드처럼 (백틱)
만약에 정말 먄약에 백틱을 써야한다면 `` ` ``처럼 해주면 됩니다. -> \`\` \` \`\`

### 코드 블록 (Code Block)*
여러줄의 코드를 표현하고 싶다면, 세개의 백틱을 활용할 수 있습니다.  

\`\`\`  
코드 블록  
\`\`\`

" ` "(백틱) 뒤 언어를 기입하는 경우 기입 언어의 표현방식을 적용합니다.

```JAVA
public class main {
    public static void main(String[] args) {
        System.out.println("Hello Java!!!");
    }
}
```
___

### 가로줄 (Horizontal Rules)

아래는 가로줄로 표현됩니다.
___
내용을 구분할때 유용합니다.
___

### 링크 (Links)
주소를 바로 링크로  
가장 간단한 링크 생성법 입니다. -> `<URL>`  
`<https://www.naver.com>` -> <https://www.naver.com>

문구에 링크 추가 -> `[링크](URL)`  
`[네이버](https://www.naver.com)`라는 글귀에 네이버 링크를 달아보았습니다.  
[네이버](https://www.naver.com)
___

### 이미지 (Images)
이미지는 아래처럼 넣어줄 수 있습니다. -> `![컴퓨터 이미지](computer.png)`
![컴퓨터 이미지](computer.png)

웹 이미지도 넣어줄 수 있습니다. -> `![Java](https://upload.wikimedia.org/wikipedia/commons/thumb/7/79/Spring_Boot.svg/120px-Spring_Boot.svg.png)`  
![Java](https://upload.wikimedia.org/wikipedia/commons/thumb/7/79/Spring_Boot.svg/120px-Spring_Boot.svg.png)
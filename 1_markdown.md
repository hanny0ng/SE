>## Table
#### 읽기의 명확성과 구문을 쉽게 분석하기 위해 권장되는 방법

	| foo | bar |
	| --- | --- |
	| baz | bim |


| foo | bar |
| --- | --- |
| baz | bim |

___

#### 길이가 일치할 필요는 없지만, 일치할 경우 쉽게 읽을 수 있음

	| abc | defghi |
	:-: | -----------:
	bar | baz


| abc | defghi |
:-: | -----------:
bar | baz

___

#### 현 파이프를 탈출해 다른 파이프까지 포함

	| f\|oo  |
	| ------ |
	| b `\|` az |
	| b **\|** im |


| f\|oo  |
| ------ |
| b `\|` az |
| b **\|** im |


___

#### 시작이 첫 번째 빈 줄 또는 다른 줄일 시 깨져보임

	| abc | def |
	| --- | --- |
	| bar | baz |
	> bar

| abc | def |
| --- | --- |
| bar | baz |
> bar

___

	| abc | def |
	| --- | --- |
	| bar | baz |
	bar
	
	bar
	

| abc | def |
| --- | --- |
| bar | baz |
bar

bar
___

#### 행은 셀 수의 구분자 행과 일치해야 함

	| abc | def |
	| --- |
	| bar |



| abc | def |
| --- |
| bar |


___

#### 헤더 행의 셀 수보다 적은 셀 수는 비어있고, 더 큰 경우 초과분은 무시됨

	| abc | def |
	| --- | --- |
	| bar |
	| bar | baz | boo |


| abc | def |
| --- | --- |
| bar |
| bar | baz | boo |


___

#### 행이 없을 시 없게 출력됨

	| abc | def |
	| --- | --- |

| abc | def |
| --- | --- |

___

>## Tasklist 

#### Tasklist는 [X] 또는 [ ]으로 구성

	- [ ] foo
	- [x] bar


- [ ] foo
- [x] bar

___

#### 임의 중첩

	- [x] foo
	  - [ ] bar
	  - [x] baz
	- [ ] bim


- [x] foo
  - [ ] bar
  - [x] baz
- [ ] bim

___

>## Strikethrough 

#### 취소선 텍스트 

	~~Hi~~ Hello, world!

~~Hi~~ Hello, world!

___

#### 새로운 문단은 취소선 X

	This ~~has a

	new paragraph~~.


This ~~has a

new paragraph~~.

___

>## autolink

#### http 자동 삽입

	www.commonmark.org

www.commonmark.org

___

#### 유효한 도메인 후 n개의 공백 문자

	Visit www.commonmark.org/help for more information.

Visit www.commonmark.org/help for more information.

___

#### 후행 구두점 (? ! . , : * _ ~)은 자동링크로 간주 X
#### 하지만 링크 내부 요소로 포함될 수 있음

	Visit www.commonmark.org.

	Visit www.commonmark.org/a.b.

Visit www.commonmark.org.

Visit www.commonmark.org/a.b.

___

#### 괄호 개수가 맞지않을 때 후행 괄호가 없다고 간주하지 않고 출력함

	www.google.com/search?q=Markup+(business)

	www.google.com/search?q=Markup+(business)))

	(www.google.com/search?q=Markup+(business))

	(www.google.com/search?q=Markup+(business)

www.google.com/search?q=Markup+(business)

www.google.com/search?q=Markup+(business)))

(www.google.com/search?q=Markup+(business))

(www.google.com/search?q=Markup+(business)

#### <br>하지만 이 검사는 닫는 괄호로 링크가 끝나는 경우에만 수행됨<br>

	www.google.com/search?q=(business))+ok

www.google.com/search?q=(business))+ok

___

#### 세미콜론으로 끝나는 경우

	www.google.com/search?q=commonmark&hl=en

	www.google.com/search?q=commonmark&hl;


www.google.com/search?q=commonmark&hl=en

www.google.com/search?q=commonmark&hl;

___

#### < = 링크를 즉시 종료

	www.commonmark.org/he<lp

www.commonmark.org/he<lp

___

#### 전자 메일

[인식 조건]
-   영숫자, 영숫자가 하나 이상,  `.`, `-`, `_`, `+` 포함
-   `@` 포함
-  영숫자 또는 영숫자인 하나 이상의 문자 `-` 또는 `_`, 기간으로 구분(`.`). 적어도 하나의 기간이 있어야 함
- 마지막 문자가 `-` 또는 `_` 중 하나일 수 없음

```markdown
foo@bar.baz
```

+가 @보다 먼저는 일어날 수 있지만 그 후는 아님

```markdown
hello@mail+xyz.example isn't valid, but hello+xyz@mail.example is.
```

. - _는 양쪽에 위치할 수 있지만 끝이 - _ 일 경우에는 주소로 간주되지 않음

```markdown
a.b-c_d@a.b

a.b-c_d@a.b.

a.b-c_d@a.b-

a.b-c_d@a.b_
```

___

>## Raw HTML

#### 아래 외의 HTML 태그는 변경되지 않은 상태로 유지된다

-   `<title>`
-   `<textarea>`
-   `<style>`
-   `<xmp>`
-   `<iframe>`
-   `<noembed>`
-   `<noframes>`
-   `<script>`
-   `<plaintext>`

#### Markdown
```markdown
<strong> <title> <style> <em>

<blockquote>
  <xmp> is disallowed.  <XMP> is also disallowed.
</blockquote>
```
#### HTML
```html
<p><strong> &lt;title> &lt;style> <em></p>
<blockquote>
  &lt;xmp> is disallowed.  &lt;XMP> is also disallowed.
</blockquote>
```

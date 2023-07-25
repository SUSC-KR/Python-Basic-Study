## 파이썬 1회차 스터디 내용 _ Python 기초

- 프로그래밍(Programing): 프로그램을 만드는 것
- 코딩(Coding) : 컴퓨터 명령코드로 작성하는 작업
- 프로그래밍 언어: 컴퓨터 프로그램 작성을 위해 고안된 언어   
<br />
- 프로그래밍 방식 종류
  * 컴파일 방식( C, C++): 번역   
  : 소스코드 → [컴파일] → 오브젝트 파일→ [링크] → 실행파일 → [실행] → 프로세스

  * 인터프리터 방식(Visual Basic, PHP): 통역   
  : 소스코드 → [인터프리터] → [실행] → 프로세스

  * JIT ( just in time ) ( JAVA, C# )   
  : 소스코드 → [컴파일] → 바이트코드 → [JVM] → [실행] → 프로세스

<br /> 
***

## 파이썬 2회차 스터디 내용 _ 자료형

- 자료형이란? 데이터를 식별하는 분류    
: 숫자형(정수,실수), 문자열, bool(참,거짓), 리스트, 튜플, 딕셔너리, 집합    
: type() -> ( ) 안에 변수 또는 데이터를 넣으면 자료형 확인 가능

<br /> 
### 1) 숫자형

- 정수(int)
- 실수(float) : 소수점이 포함된 숫자(실수는 정수를 제외한 실수만을 의미)
- 진법(진수)
<br />

- 산술연산자
  * / * + - : 사칙연산
  * ** : 거듭제곱
  * // : 몫,  %: 나머지

- 복합대입연산자
  * += : a += b → a = a + b
  * -= : a -= b → a = a - b
  * *= : a *= b → a = a * b
  * /= : a /= b → a = a / b   

<br /> 
※ 변수   
: 값을 저장할 수 있는 공간   
( 여러 번 저장 가능, 마지막에 저장된 값으로 변경됨)​

- 변수 선언 규칙
  1. 중복된 이름은 변수로 사용X
  2. 변수 명은 영문자, 숫자, 언더바( _ )만 사용
  3. 변수 명의 첫 문자는 반드시 영문자 or 언더바( _ )
  4. 예약어는 변수 명으로 사용 불가능 ex. if, break, False...
  5. 변수 명은 대소문자 구분 가능
  6. 변수 명 내에 공백 불가능

<br />

- 변수명 = 데이터 값   
→ 데이터 값이 변수 명에 저장된다

<br /> 
### 2) 문자열

- 대입
  * " " (쌍따옴표) or ' ' (홑따옴표)로 데이터 대입
  * 여러 줄인 문자열 데이터는 " " " (쌍따옴표 3개) or ' ' ' (홑따옴표 3개)로 대입   
  <br />
- Escape Sequence (이스케이프 문자)
  * \n : 줄바꿈
  * \t : tap
  * \\ : 문자 \ 그대로 표현
  * \' : 홑따옴표 그대로 표현
  * \" : 쌍따옴표 그대로 표현   
  <br />
- 문자열 연산
  * 문자열 더하기: a = ‘hi’ , b = ‘python’ , print(a+b) = hipython
  * 문자열 곱하기(복제): c = "good day" , print(c*3) = good daygood daygood day   
  <br /> 
- 인덱싱(indexing) : 문자열 내에 단일 문자들은 각각 번호가 있다   
ex. a = "Welcome to Python"  ⇒ a[0] = 'W' , a[11] = 'P' , a[-13] = 'o'

<br /> 
- 슬라이싱(slicing) : 문자열을 필요한만큼 자른다   
[start :end -1: step] → start: 시작, end-1 : 마지막 위치, step: 건너뛰기   
ex. a[8:] = 'to Python' , a[:] = 'Welcome to Python', a[0:9], a[0:]...   
<br /> 
- 포매팅 : 문자열 내에 공간을 만들고 사용할 때마다 원하는 값 넣을 수 있다
  * %s : 문자열(String)
  * %c : 문자 1개(Character)
  * %d : 정수(Integer)
  * %f : 부동소수(Floating-point)
  * %o : 8진수
  * %x : 16진수
  * %% : Literal %(문자%자체)   
ex. 문자열 바로 대입 ⇒ print("I eat %s cakes"%"two")   
ex. 변수 이용해 대입 ⇒ a = 3, print("I eat %d cakes"%a)
  * 정렬 ⇒ ex. "%10s" % "hi"  >> '          hi'
  * 공백 ⇒ ex. "%-10shello" % "hi" >> 'hi          hello'
  소수점 ⇒ ex. "%10.4f" % 3.141592 >> '        3.1415'

  * format
    + 숫자 바로 대입: print("I eat {0} apples".format(3)) >> 'I eat 3 apples'
    + 문자열 바로 대입: print("I eat {0} apples".format("five")) >> 'I eat five apples'
    + 변수 값 대입: a=“h”,b=“U”, print("I {0}, i {1}".format(a,b)) >> 'I h , i U'
    + 이름 사용 가능: print("hi {python}".format(python = 10)) >> 'hi 10'

<br /> 
- 문자열 내장함수

  ex. a = " happy "   
  '''python
  a = " happy "   
  print(a.count('p')) = 2  # 문자 개수 세기   
  print(a.find('y')) = 4  # 위치 알려줌   
  print(a.index("h")) = 0  # 위치 알려줌   
  print(a.join("abc"))  # 문자열 삽입   
  print(a.lower())  # 소문자로 변환   
  print(a.lstrip()) = "happy "  # 왼쪽 공백 지우기   
  print(a.rstrip()) = " happy"  # 오른쪽 공백 지우기   
  print(a.strip()) = "happy"  # 양쪽 공백 지우기   
  print(a.replace("ha","po")) = "poppy"  # 문자열 교체   
  print(a.split())  # 문자열 나누기   
  print(a.center(30))  # 문자열 정렬   
  print(a.ljust(30))  # 문자열 왼쪽 정렬   
  print(a.rjust(30))  # 문자열 오른쪽 정렬
  '''

<br /> 
### 3) 리스트
: 여러 값을 하나의 변수에 넣음(목록)   
<br />
※ 형식   
리스트 명 = [요소1, 요소2, 요소3 … ]

- 리스트 변수 선언 종류
  * 비어있는 리스트 : a = [ ]   
  * 정수형 리스트: b = [ 1 , 2 , 3 ]   
  * 문자열 리스트: c = ["like" , "python"]   
  * 정수+문자열 : d = [ 1 , 2 , "like" , "python" ]   
  * 정수+리스트: e = [ 1 , 2 , ["like" , "python"]]   
<br /> 
- 리스트 인덱스   
ex) a = [ 1 , 2 , "like" , "python" ]   
print(a[0]) = 1 / print(a[0]+a[1]) = 3 / print(a[3][1]) = y   
<br /> 
- 리스트 수정/삭제
  * 수정: a = [1,2,3] → a[2] = 4 → print(a) = [1,2,4]
  * 삭제: a = [1,2,3,4,5] → a[1:3] = [ ] → print(a) = [1,5]   

<br /> 
※ del 함수: 객체 삭제할 때 사용   
ex) a = [1,2,3,4,5] → del a[1] → print(a) = [1,3,4,5]   
(일반 숫자형 변수 삭제도 가능 ex. a = 5 → del a )   
<br /> 
but>> 문자열은 인덱싱으로 삭제 불가능: a = "hi" → del a 가능, del a[0] 불가능!   
<br /> 
- 리스트 내장 함수( 리스트a → a.함수() 이렇게 사용 )
sum() = 리스트 요소들의 합   
max() = 리스트 요소 중 가장 큰 값   
min() = 리스트 요소 중 가장 작은 값   
len() = 리스트 요소의 개수(길이)    
zip () = 2개의 리스트 받아서 하나로 묶어서 제공   
append() = 요소추가 ex) a = [1,2,3] → a.append(4) → [1,2,3,4]   
sort() = 정렬   
reverse() = 뒤집기 ex) a.reverse() = [3,2,1]   
index() = 위치찾기 ex) a.index(3) = 2   
insert() = 요소 삽입 ex) a.insert(0,4) - [4,1,2,3]   
remove() = 요소제거   
extend() = 리스트확장   
count() = 개수세기   
pop() = 요소 끄집어내기   
clear() = 모든 항목 삭제   
copy() = 복사본 반환  

<br /> 
// 추가   
"value" in mylist : value가 mylist에 있으면 True   
"value" not in mylist : value가 mylist에 없으면 True   
<br /> 

- 리스트 복사하기
1. 얕은 복사   
'''python   
x_list = [ 1, 2, 3, 4, 5 ]   
y_list = x_list   
y_list[2] = 30   
print(x_list) = [ 1, 2, 30, 4, 5 ]   
'''   
→ 같은 주소를 '공유'하도록 복사했기 때문에 y_list를 변경하면 같은 주소를 갖고있는 x_list도 바뀜   
<br /> 

2. 깊은 복사   
'''python   
x_list = [ 1, 2, 3, 4, 5 ]   
y_list = list(x_list) → list()는 리스트 객체의 생성자 (객체를 생성하고 초기화하는 함수)   
'''
<br /> 
⇒ 다른 객체들을 받아서 리스트로 변환! (y_list가 바뀌어도 x_list는 그대로)   
<br /> 

- 리스트 슬라이싱
1. list [ start : stop ]   
ex) a = [ 1, 2, 3, [’a’ , ‘b’ , ‘c’ ] , 4 ]   
print(a[0:2]) / print(a[3][:2])

2. list [ start : stop : step ]   
ex) a = [ 1, 2, 3, 4, 5, 6, 7, 8, 9 ]   
print(a[::2]) = [1, 3, 5 ,7, 9] / print(a[1::2]) = [2, 4, 6, 8]   
<br /> 

※ 리스트 연산은 문자열과 동일하다( + , * 만 가능)   
: 정수+문자열은 문법 오류 → str() 로 형변환   
<br /> 

- 리스트 함축   
형식: 리스트변수 = [ 출력식 for x in 리스트 if 조건 ]

ex1.  
'''python   
squares = [ ]   
for x in range(10):   
  squares.append(x*x)   

⇒ squares = [ x*x for x in range(10) }   
'''   
<br /> 

ex2. 0~9까지 정수 중 짝수면 "짝수"를 리스트에 추가하고, 홀수이면 "홀수" 추가하는 리스트 함축

⇒ '''python   
number = [ x for x in range(10) if x % 2 == 0 and x % 3 == 0 ]   
'''   
<br /> 

### 4) 튜플 tuple
: 리스트와 거의 동일함   
튜플 명 = ( 요소1, 요소2, 요소3 ... )   
<br /> 

※ 차이점   
① 리스트는 대괄호 [ ] 로 요소를 감싸지만 튜플은 소괄호 ( ) 로 감싸준다   
② 리스트는 요소의 수정, 삭제가 가능하지만 튜플은 한번 값을 넣으면 바꿀 수 없다   
<br /> 

- 튜플 선언
t1 = ()   
t2 = (1,)   → 값을 하나만 넣을 땐 값 뒤에 ' , ' 사용   
t3 = (1, 2, 3)   
t4 = 1, 2, 3    → 괄호 생략 가능   
t5 = ('a', 'b', ('ab', 'cd'))   
<br /> 

※ 튜플>> 인덱싱, 슬라이싱, 연산 가능   
※ 튜플은 요솟값을 변경할수 없기 때문에 sort, insert, remove, pop과 같은 내장 함수가 없음   
<br /> 

### 5) 딕셔너리 dictionary
: 여러 개의 값을 넣고 각 요소에 이름을 부여함   
딕셔너리 명 = { Key1 : Value1, Key2 : Value2, Key3 : Value3 ... }   
<br /> 

※ 딕셔너리는 중괄호 { } 사용   
<br /> 

- 딕셔너리 쌍 추가   
a = { 1 : 'a' }   
a[2] = 'b'   
a >> { 1 : 'a' , 2 : 'b' }   
a['name'] = 'pey'   
a >> { 1 : 'a' , 2 : 'b' , 'name' : 'pey' }   
a[3] = [1,2,3]   
a >> { 1 : 'a' , 2 : 'b' , 'name' : 'pey' , 3 : [1,2,3] }   
<br /> 

- 요소 삭제   
del a[1]   
a >> { 2 : 'b' , 'name' : 'pey' , 3 : [1,2,3] }   
<br /> 

- key 이용해서 value 얻기   
age = { 'park' : 23 , 'kim' : 24 }   
age['park'] >> 23   
age['kim'] >> 24   
<br /> 

※ 딕셔너리는 인덱싱 적용 불가능   
a = { 1 : 'a' , 2 : 'b' } 일 때,   
a[1] = 'a' → 인덱싱이 아니라 key에 해당하는 1을 나타낸 것   
<br /> 

※ 딕셔너리는 중복된 key 값을 사용할 수 없음(value는 가능)   
<br /> 

- 딕셔너리 내장 함수   
food = { "김치찌개" : 7000, "김밥" : 1000, "떡볶이" : 500 }   
<br /> 

① key 리스트 만들기(keys)   
food_menu = list(food.key())   
print(food_menu) >> [ '김치찌개', '김밥', '떡볶이' ]   
<br /> 

② value 리스트 만들기(values)   
food_price = list(food.values())   
print(food_price) >> [ 7000, 1000, 500 ]   
<br /> 

③ key, value 쌍 리스트 만들기(items), 쌍 리스트 지우기(clear)   
<br /> 

④ key로 value 얻기(get)   
food.get('김치찌개') >> 7000   
<br /> 

⑤ 해당 key 있는지 찾아보기(in)   
print('김밥' not in food) >> False   
print('배고파' in food) >> False   
<br /> 

### 6) 집합 set
: 집합에 관련된 데이터들을 쉽게 처리하기 위해 만들어진 자료형(숫자에 특화돼있음)   
<br /> 

※ 집합은 순서가 없다   
※ 집합은 중복을 허용하지 않는다 → 중복 제거하기 위한 필터로 종종 사용됨   
※ 순서가 없으므로 인덱싱이 불가   
  ( 인덱싱으로 접근하고 싶다면 리스트 or 튜플로 변환 후 사용)   
  s1 = set( [ 1, 2, 3 ] )   
  s2 = list(s1)   
  s2 >> [ 1, 2, 3 ]   
<br /> 

- 교집합 구하기   
s1 = set([ 1, 2, 3, 4, 5, 6 ])   
s2 = set([ 4, 5, 6, 7, 8, 9 ])   
s1 & s2 >> { 4, 5, 6 }  ⇒ & 이용   
s1.intersection(s2) >> { 4, 5, 6 }  ⇒ intersection 함수 이용   
<br /> 

- 합집합   
s1 | s2 >> { 1, 2, 3, 4, 5, 6, 7, 8, 9 }  ⇒ | 이용   
s1.union(s2) >> { 1, 2, 3, 4, 5, 6, 7, 8, 9 }  ⇒ union 함수 이용   
<br /> 

- 차집합   
s1 - s2 >> { 1, 2, 3 } / s2 - s1 >> { 8, 9, 7 } ⇒ - (마이너스) 이용   
s1.difference(s2) >> { 1, 2, 3 } / s2.difference(s1) >> { 8, 9, 7 } ⇒  difference 함수 이용   
<br /> 

- 집합 내장 함수   
add() = 요소추가   
update() = 요소 여러개 추가   
remove() = 요소 삭제   
<br /> 
​
#### 블로그링크
- python 프로그래밍 기초: <https://blog.naver.com/wivkfm00/223096573141>
- 자료형&변수_(1) 숫자형, 문자열: <https://blog.naver.com/wivkfm00/223097452157>
- 자료형&변수_(2) 리스트: <https://blog.naver.com/wivkfm00/223098550251>
- 자료형&변수_(3) 튜플, 딕셔너리, 집합: <https://blog.naver.com/wivkfm00/223098613806>

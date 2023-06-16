# python 

## 01.type
```
int()    :  정수
type()   :  종류 알려줌
id()     :  저장된 위치
dir()    :  사용가능한 명령어 정리 ,객체의 속성, 메서드 확인
float()  :  실수 
str()    :  문자열
2진수    :  0b
8진수    :	0o
16진수   :  0x
bool     : 논리 True (모든 숫자 0제외) , False (0일때)
complex  : 복소수, real + imaginary (실수부 + 허수부 j)
enumerate : (index, value) 주소와 값 출력함
객체 : class를 가지고 memory에 구현한 구현체
strip() : 문자 앞뒤 공백 제거
split() : 공백 구분자로 분리


```
### 관리 객체
 `list : 순서 o , 중복 o`
```
a = [5,4,3,2,1]
b = list()
b.append()
b.reverse
b.sort
b.insert(4, 6) : index 4 위치에 6삽입
len(b)
list[index] : b[1] 
```

`tuple : 순서 o , 중복 o (수정 불가)`
```
a = (5,4,2,1)
b = tuple([4,3,2,1]) : list->tuple
b.count : 값 개수
list(b) : tuple -> list
packing : f = 1, 2, 3
unpacking : g, h, i = f
```

> `set : 순서 x , 중복 x`
```
실행 할때마다 순서 변경. 문자열도 다 섞임
b = {1,2,3,4,5} : 숫자 값이 주소 값으로 정의됨.
c = set([1,2,3,4,5]) 
c.add('6')
c.pop() : 가장 앞에 있는 문자 출력 (매번 다름)
forzenset([1,2,3,4,5]) : 위치 고정

합집합 : left.union(right) , left | right
교집합 : left.intersection(right) , left & right
차집합 : left.difference(right) , left - right
```

> `dit : 순서 o , 중복 (key : x, value : o) `
```
dit01 = {'a': 1, 'b': 2, 'c': 3}
dict02 = dict(a=1, c=2, b=3)
dict03 = dict([[1, 'a'], [2,'b']])

list(dit03.keys()) -> [1,2]
dit03.values()
```

> `mutable : 값이 변화 해도 주소값 변화 x` 
- list, dicionary, set

> `immutable : 값이 주소값`
- numbers, tuple, str, frozenset

> `str : text sequence`
```
\'  \' , ' " " ': 문자열 속 따옴표 , 싱글속 더블 or 더블속 싱글 
'''    '''      : 여러줄 문자열 
r' ' : r뒤에 전부 문자열
\n : 줄 건너뛰기
\t : tab

```
> `print : 출력 -> print('name', name, sep=":", end="\t")`
```
sep : , 기준으로 " "-> 삽입
end : 끝낫을 떄 \n : 줄바꾸기 , \t : tab , 공백 등 삽입 
print(f'asdsad {sdsad}') -> sdsad 변수 삽입
```

## 02.operation
### `range( )`
```
list(lange(10,0,-1)) :[10, 9, 8, 7, 6, 5, 4, 3, 2, 1]
slice : [start, stop, step] -> start index ~ stop index-1
start,stop 생략하면 끝까지!
```

## 03.control 뒤에 :
### `if 조건 : (중첩 가능)`
```
b=1,c=2
if b> c:
    print(f'{b} > {c}')
elif b < c:
    print(f'{b} < {c}')
else:
    print(f'{b} == {c}')

# 비어있는 문자열은 False ,[], {}, () , None,0 모두 false

```
### `match`
```
# match 뒤엔 식 또는 값이 들어감.
match season:
    case 12 | 1 | 2:
        print("겨울")
    case _:  ( _: 값을  사용하고 싶지 않을 때, 나머지 숫자)
        print("1~12 사이의 값을 입력해 주세요!")
```
### `for`
```
# for 변수 in collection:
# collection : list, tuple, set, dict, ...
# iterable 반복가능한 객체들 (), (__iter__, __next__)
```
### `while 조건 :`
```
# 해당 조건이 Ture인 동안 반복
else:  # 반복문이 정상적으로 모두 수행 되었을 때 실행
```
### `break `
```
break
for i in range(10):
    if i > 5:
        break # false되면 else 실행 x
    print(i, end=" ")
else:
    print("5까지 출력?")
```
### `Continue`
```
for i in range(10):
    if i % 2 == 0:
        continue # 아래 명령문을 무시하고 다음 반복으로 진행 
        (false 일때 print(i) 무시하고 다음 반복 진행)
    print(i, end=" ")
```
### `한줄로 표현`
```
list02 = [i for i in range(1, 11)]
list03 = [i for i in range(1,11) if i % 2 ==0]
```

## 4. function
```
def hello05():
    return 1
#   return 2 여기까지 도달 x
#   return 3 여기까지 도달 x
```
- parameter : 함수 외부에서 전달되는 값을 받아서, 함수 내부에서 사용하기 위한 "변수"
- arguments : 함수 외부에서 전달되는 "값"
- *args : 여러 개의 값을 한 번에 받을 수 있음!
- **kwargs: ** -> k=v 형태로 가지고있을거야
- lambda : 익명 함수 표현식

> 변수
- 전역 변수 : 전체 영역에서 사용됨
- 지역 변수 :  들여 쓰기 되어 있는 영역에 변수는 지역 변수, 함수 내에서만 사용됨

- nonlocal : 바로 하나 위에 있는 지역 변수 사용
- global : 함수내에서 전역 변수 사용할떄. 바꿔버리기 가능 (지역 변수는 x)

### `clouser`
```
lexical scope  :  함수가 선언 될 때, 변수의 범위(scope)가 정해진다.
```

### `재귀함수`
```
def factorial_recursion(n):
    # 종료 조건 필수 !
    if n == 1:
        return 1

    return n * factorial_recursion(n-1)

나를 다시 호출
```

## 05. module
```
module ~= library 누군가 만들어놓은 기능 배포
import 호출 기능
import sys  : 내장 모듈
import name -> name.def()
import math as m -> math 대신 m으로 사용가능
```
### `datetime`
```
date : 날짜
datetime : 날짜 + 시간
timedelta : 날짜 계산
```

### `import re` : regular expression (정규 표현식, 정규식)
```
. : 문자 1개
^ : 문자열의 시작
$ : 문자열의 마지막
* : o or more
+ : 1 or more
? : 0 or 1
{n} : n번 반복
{n,m} : n번 부터 m번
{n,} : n번 부터 무한번
[] : 문자의 집합
| : OR
() : 괄호 안의 정규식 그룹

\w : [a-zA-Z0-9_] : a~Z, 0~9, _ 포함하는 모든 문자
\W : [^a-zA-Z0-9_] : 위의 문자 제외한 나머지 문자
\d : [0-9] : 0 부터 9
\D : [^0-9] : 숫자 제외한 나머지 문자
\s : [\t\n\r\f\v] : 공백문자
\S : [^\t\n\r\f\v] : 공백 제외한 모든 문자
\b : 단어의 시작과 끝의 빈 공백
\B : 단어의 시작과 끝이 아닌 빈 공백
\\ : \
\[숫자] : 지정된 숫자만큼 일치하는 문자열
\A : 문자열의 시작
\Z : 문자열의 끝
```

## 06.io -> input , output
```
file = open('file.txt', 'w')
file.close() -> open 후 close 필수
r : 읽기
w : 쓰기 (기존 내용 덮어쓰기)
a : 쓰기 (기존 내용 이어서 쓰기)
x : 쓰기 (새로운 파일 만들어서 쓰기)
t : text
b : binary -> binary로 저장.
```

## 07.class : 객체를 만드는 애 , 설계도 
```
낙타 표기법, 단어 구별을 대문자로 ,첫글자도

특징
- 추상화
공통점을 묶어놓은 것

- 상속
묶어 놓은 것을 가져와서 사용함

- 다형성
여러가지 형태로 만들어짐

- 캡슐화
코드를 은닉한 상태로 배포하여 사용할 수 있음
 module / import를 통해

```

```
속성 : variable (class 변수, instance 변수)
기능 : function, method
    -@classmethod : (cls) -> 호출하는 class 값
    -@staticmethod : ! 정적으로 사용
    -instance method : self 나 자체가 가진 인스턴스 변수 사용


__??__ : special method, magic method
__init__ : 객체 생성 시, 인스턴스 변수 초기화
self.변수 -> instance vaiable , 나 객체 자신.
______() -> 객체 생성
객체 : class를 가지고 memory에 구현한 구현체
 () 붙히는 이유: 생성자 호출 의미
 # 객체마다 다른 값을 가지고 있어야하면 인스턴스 변수
 # 객체마다 같은 값을 가지고 있어야하면 클래스 변수
 # __ 필수 : 외부에서 건드릴 수 없는.
 ```
 > getter : 외부 (설계도class 밖)에서 받아옴

 > setter : 외부 (설계도 밖)에서 세팅
 
 > `데코레이터` # self 안받음 # 객체 상관없이 공통적인 기능
 instance 변수 사용 불가 

 > `del` : 해당 변수 지우기. 연결된 값도.

 ### Parent 
 ```
 # 자식이 부모 객체 사용가능 하다
 # self. 부모가 가진 값은 못가지고 옴
 super() : parent 안에 있는 object.
 # __new__ 없어도 Object가 만들어 놓음.
 # override : 부모의 메서드를 가져다가 재정의

 @staticmethod # parameter에 아무거나 넣을 수 있음
 @classmethod # 원래와 다른점 : cls
 ```
 ### 상속
 ```
 class Griffin(Lion,Eagle): # 다중 상속하고 있음

 class Child(Father, Mother): # 다이아몬드 상속
    # 아빠 먼저 상속을 받아 아빠출력함
    # 아빠가 비어있다면 엄마, 둘다 비어있을 경우에 Person
    pass
/father, mother 의 부모인 person
 override 시 문제 생길 수 있다.
Method Resolution Order (MRO) : 메서드 탐색 순서
```

### 추상
`@abstractmethod` : abc (Abstract base class)
```
# 내용이 비어있는 것 : 추상 메서드
# 껍데기만 있는 것
# 아직 무슨 내용을 추가 할지 모를 때
# 추상 클래스는 객체화 불가!

자식이 반드시 구형해야함.
```

### `metaclass` : class 만들어주는 class


### `singleton pattern` : 객첼르 한번만 만들고 싶어요!
 (= 메모리에 객체 하나만 생성)

### `from abc import *` # == import abc 같지만 abc. 안붙혀도 됨

## `special method`
```
# __ge__() : >=
# __gt__() : >
# __le__() : <=
# __lt__() : <
# __eq__() : ==
# __ne__() : !=

# __add__() : +
# __sub__() : -
# __div__() : /

# __new__(), __init__() : 생성자
# __str__() : 객체 표현
# __repr__() : 객체 표현

# __str__ 지우면 __repr__작동

eval : 명령 실행

def __call__(self, name) :  객체를 함수처럼 사용 가능


```
```
@property : class 외부에서 변수의 값을 호출하기 위한 함수
@변수.setter : class 외부에서 변수에 값을 대입하기 위한 함수
@classmethod : method를 호출한 class의 변수를 사용하는 method
@staticmethod : super class의 변수를 사용하는 method
```

## 08. `Decorater` : 기능을 추가 하기 위한 syntax sugar

```
#1 함수가 값으로 전달됨
#2 outer()
#3 inner함수가 값
#4 inner()

# Greeting(myfunc)() # (),__call__-> 객체를 함수처럼 쓸수 있다.
```

## 09. `exception` : 예외가 발생했을 때 프로그램의 강제 종료 방지
```
try:
    # 에러가 발생할 가능성이 있는 코드:
    print(10/0) 
    pass

except:
    # exception을 catch! (에러가 발생했을 시, 수행할 코드)
    print('예외 발생')
    pass

else:
    # 에러가 발생하지 않으면 수행할 코드
    pass
finally:
    # 발생 여부와 상관 없이, 무조건 수행할 코드
    pass
```
> except `Exception` as e: #예외 최상위 옵션 Excetion

### `MyException` : 특정 상황에 에러 일으키고 싶을 떄, raise 사용
```
raise -> 일으키다
```

## 10.`iteratior`
```
# iterable : 반복 가능한 ( 값을 순서대로 꺼내올  수 있는)
# iterator : 반복 (값을 순서대로 꺼내는) 객체
# lazy evaluation : 실행될 때 연산
# __iter__() : iterator반환
# __next__() : iterator 내부의 값 하나 변환
```

## 11.`generator` : 요청 들어오면 만들어서 제공 후 대기

```
yield : 외부로 값 전달
__next()__ : 호출될 시 외부로 전달
```
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
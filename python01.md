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
```
### 관리 객체
> list : 순서 o , 중복 o
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

> tuple : 순서 o , 중복 o (수정 불가)
```
a = (5,4,2,1)
b = tuple([4,3,2,1]) : list->tuple
b.count : 값 개수
list(b) : tuple -> list
packing : f = 1, 2, 3
unpacking : g, h, i = f
```

> set : 순서 x , 중복 x
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

> dit : 순서 o , 중복 (key : x, value : o) 
```
dit01 = {'a': 1, 'b': 2, 'c': 3}
dict02 = dict(a=1, c=2, b=3)
dict03 = dict([[1, 'a'], [2,'b']])

list(dit03.keys()) -> [1,2]
dit03.values()
```

> mutable : 값이 변화 해도 주소값 변화 x 
- list, dicionary, set

> immutable : 값이 주소값
- numbers, tuple, str, frozenset

> str : text sequence
```
\'  \' , ' " " ': 문자열 속 따옴표 , 싱글속 더블 or 더블속 싱글 
'''    '''      : 여러줄 문자열 
r' ' : r뒤에 전부 문자열
\n : 줄 건너뛰기
\t : tab

```
> print : 출력 -> print('name', name, sep=":", end="\t")
```
sep : , 기준으로 " "-> 삽입
end : 끝낫을 떄 \n : 줄바꾸기 , \t : tab , 공백 등 삽입 
print(f'asdsad {sdsad}') -> sdsad 변수 삽입
```

## 02.operation
> range()
```
list(lange(10,0,-1)) :[10, 9, 8, 7, 6, 5, 4, 3, 2, 1]
slice : [start, stop, step] -> start index ~ stop index-1


```
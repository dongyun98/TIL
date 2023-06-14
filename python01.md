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
bool     : 논리 True , False
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

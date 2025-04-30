<div align="center">

# Deep Dive  
Deep Dive into Java

--- 
</div>

## Contents
- [Null](#null)
- [GC](#GC)

### Null
참조형 변수에는 항상 객체가 있는 위치를 가르키는 참조값이 들어간다. 하지만 아직 가르키는 대상이 없거나, 가르키는 대상을 나중에 입력하고 싶을 땐 Null을 사용한다.

- Null의 할당 
```
null 지정
Data d1 = null;

메모리 할당
d1 = new Data();

null 지정
d1 = null
```

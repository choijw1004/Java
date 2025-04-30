<div align="center">

# Deep Dive  
Deep Dive into Java

--- 
</div>

## Contents
- [Null](#null)
- [GC](#GC)
- [NullPointerException](#nullpointerexception)

### Null
참조형 변수에는 항상 객체가 있는 위치를 가르키는 참조값이 들어갑니다. 하지만 아직 가르키는 대상이 없거나, 가르키는 대상을 나중에 입력하고 싶을 땐 Null을 사용합니다.

- Null의 할당 
```
null 지정
Data d1 = null;

메모리 할당
d1 = new Data();

null 지정
d1 = null
```

### GC
> d1에 null을 할당하면 기존 생성했던 Data()는 참조값을 다시 구할 방법이 없습니다. 따라서 인스턴스에 메모리에 필요없는 부분이기 때문에 Java에서는 자동으로 메모리에서 제거됩니다. 

### NullPointerException
만약 참조값 없이 객체를 찾아가면 어떤 문제가 생길까요? 이 경우 발생하는 에러가 NullPointerException이 발생합니다. 객체를 참조할 때는 .(dot)을 사용하지만 참조할 수 없다면 에러가 발생합니다. 
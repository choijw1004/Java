<div align="center">

# Deep Dive  
Deep Dive into Java

--- 

</div>

## Contents
[기본형과 참조형](기본형과-참조형)

--- 

### 기본형과 참조형
Java에서는 사용하는 값을 직접 넣을 수 있는 ```기본형```과 ```참조형```으로 분류가 됩니다.
- 기본형: int, long, double, boolean
실제 사용하는 값을 변수에 담을 수 있습니다.
- 참조형: Student stu1, int[] students
객체의 위치(참조, 주소)를 저장합니다. 

#### 변수 연산
 기본형은 연산이 가능하지만 참조형은 연산이 불가능합니다.
 ```
 int a = 10;
 int b = 10;

int c = a + b;
 ```
.(dot)을 통해 객체의 기본형 멤버 변수에 접근한 경우에는 연산을 할 수 있습니다.
```
Student s1 = new Student();
Student s2 = new Student();
int sum = s1.grade + s2.grade;
```

> Java에서 String은 사실 클래스입니다. 참조형이지만 기본형 처럼 문자 값을 바로 대입할 수 있습니다. 

#### 변수 대입
- 기본형 대입
```
int a = 10;
int b = a;
```
- 참조형 대입
```
Student s1 = new Student();
Student s2 = s1;
```
> 참조형의 경우 실제 사용하는 객체가 아니라 객체의 위치를 가리키는 참조값만 복사됩니다. 

#### 메서드 호출  
- 기본형과 메서드 호출
```
int a = 10;
change(a);

method change(int a){
    a = 20;
}
print(a) 
```
- 참조형과 메서드 호출 

```
Data d1 = new Data();
d1.value = 10;

method change(Data d){
    d.value = 20;
}
```

> 기본형에서 메서드 호출할때 파라미터에 int a를 전달하게 되면 a의 변수값을 복사해서 대입하는 것이고, 참조형의 경우 Data d의 파라미터를 전달하는 주소값을 전달하기때문에 원본 객체에도 적용되게 된다.
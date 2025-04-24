<div align="center">

# Deep Dive  

--- 
</div>

## Contents
- [클래스가 필요한 이유](#클래스가-필요한-이유)
--- 
### 클래스가 필요한 이유 
Java의 클래스와 객체는 가장 중요한 주제입니다. 

먼저, 클래스가 왜 필요한 지 하나의 코드를 작성해보겠습니다.

```
String stu1Name = "학생 1";
int stu1Age = 15;
int stu1Grade = 90;
    
String stu2Nmae  = "학생 2";
int stu2Age = 16;
int stu2Grage = 80;
```

두 명의 학생을 위와 같은 방식으로 선언하는 경우에는 학생이 추가되거나, 기존에 있는 학생의 정보를 수정하는 경우에는 일일히 학생의 정보를 찾아서 삽입, 삭제하는 과정을 거쳐야합니다.

그렇다면 아래와 같은 방식으로 이 코드를 변경해보겠습니다.

```
String stu1Name = "학생 1";
int stu1Age = 15;
int stu1Grade = 90;

String stu2Nmae  = "학생 2";
int stu2Age = 16;
int stu2Grage = 80;

String[] studnetNames = {"학생1", "학생2"};
int[] stuAges = {15,90};
int[] stuGrades =  {90,90};
```

기존의 이름과, 나이, 성적을 배열로 묶어 인덱스 별로 관리해보았습니다. 
하지만 이 방법은 당연하게 한 명의 학생의 삭제과정이 발생하는 경우 다른 배열들의 인덱스를 함께 지워야 하는 매우 위험해집니다.

### 클래스의 도입
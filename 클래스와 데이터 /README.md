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
위와 같이 한 명의 학생의 이름, 나이, 성적을 일일히 관리하는 방법 대신에 클래스를 도입하여 한 명의 학생을 하나의 객체로 작성할 수 있다면 위에 제기한 문제를 해결할 수 있을 것입니다.

```
public Class Student{
    String name;
    int age;
    int grade;
}
```

- 클래스의 멤버 변수는 name, age, grade와 같은 필드입니다.
- 클래스는 관례상 camelCase를 사용합니다.  

클래스를 선언한 다면 아래와 같이 쓸 수 있습니다.

```
Student stu1 = new Student();
stu1.name = "장우"
stu1.age = 29;
stu1.grade = 100;
```

stu1이라는 인스턴스를 메모리에 적재해준 후 name, age, grade를 설정합니다. 단순히 보기만 해도 코드의 양, 효율성이 높아진 것을 확인할 수 있습니다. 

Student라는 사용자 정의 타입을 설정했습니다. Student라는 설계도를 직접 정의하여 내부의 이름, 나이, 성적을 명시하였습니다. 

위의 코드에서는 Student라는 설계도를 사용하여 메모리에 적재 후 stu1이라는 인스턴스를 만들어내는 과정입니다.

객체를 생성하면 Java는 메모레의 어딘가에 객체에 접근할 수 있는 참조 주소를 반환하게 됩니다. 반환한 참조 주소는 생성된 인스턴스에 함께 저장되게 됩니다. 
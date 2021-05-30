---
title: "Refelction & Annotation"
excerpt: "JAVA의 Reflection과 Annotation에 대해서 알아본다."
categories:
- CS
tags:
- JAVA
- CS
- Reflection
- Annotation
---

### 리플렉션, Refelction

실행시간에 객체의 내용을 조사하고, 해당 객체의 메소드를 호출할 수 있다.



클래스를 구성하는 요소와 java.lang.reflect 패키지 클래스

- 멤버 변수, 필드 - Field
- 메소드 - Method
- 생성자 - Constructor



### Class 클래스

**어떤 클래스의 모양(구성)을 알고 있는 클래스**

- Fields
- Methods
- Constructors
- 상속 받은 것
- 인터페이스 등



**getClass 메소드를 통해 클래스를 나타내는 객체를 얻을 수 있다.**

```java
Object obj = ... ;
Class<?> clazz = obj.getClass();
```

- getDeclaredField(String name) - Field
- getDeclaredFields() - Field[]
- getDeclaredMethod(String name) - Method
- getDeclaredMethods() - Method[]
- getDeclaredConstructor(Class<?> ...paramTypes)
- getDeclaredConstructors() - Constructor



### 애너테이션, Annotation

**애너테이션이란?**

- 사전적 의미는 주석이다.
- @를 이용한 주석, 자바코드에 주석을 달아 특별한 의미를 부여한 것이다.
- 코드에 정보를 추가하는 정형화된 방법



**애너테이션 사용 용도**

1. @Override 애너테이션처럼 컴파일러를 위한 정보를 제공하기 위한 용도
2. 컴파일 과정에 애너테이션 정보로부터 코드를 생성하기 위한 용도
3. 스프링 프레임워크의 @Controller 애너테이션처럼 런타임에 리플렉션을 이용해서 특수 기능을 추가하기 위한 용도



**JDK 제공 기본 애너테이션**

- @Override

  해당 메소드가 부모 클래스에 있는 메소드를 재정의했다는 것을 명시적으로 선언

- @Deprecated

  더 이상 사용되지 않는 클래스나 메소드 앞에 추가

- @SuppressWarnings

  컴파일러의 경고를 무시하라고 프로그래머에게 알려줌



### 애너테이션 작성

**@interface 키워드로 정의**

```java
public @interface TestAnnotation {
}
```

```java
import java.lang.annotation.*;

@Target(ElementType.TYPE) // 클래스 수준에서 사용 가능 (생략하면 어디든 사용 가능)
@Retention(RetentionPolicy.RUNTIME) // 컴파일 단계에서 사용할 것인지 런타임 시에도 사용할 것인지
@Documented // java doc 으로 documentation에 포함시키게 됨.
public @interface TestAnnotation {
}
```



**메타 애너테이션**

어노테이션을 선언할 때 사용한다.



### 어노테이션 적용 대상

**@Target (디폴트는 모든 대상)**

- Type : 클래스 레벨에 지정 가능
- Field : 멤버 변수 레벨에 지정 가능
- Method : 메소드 레벨에 지정 가능
- Parameter : 파라미터 레벨에 지정 가능
- Constructor : 생성자 레벨에 지정 가능
- Local_variable : 지역 변수 레벨에 지정 가능



**@Retention**

- source : 컴파일 시에 사용되고 무시된다.
- class : 기본값 클래스파일에 기록되고, jvm에 로드되지 않는다.
- runtime : 클래스파일에 기록되고, jvm에 의해 로드된다.



**@Documented**

- Java Docs에 포함 될 것인지를 선언



**@Inherited**

- 모든 자식 클래스가 부모 클래스의 어노테이션을 사용 가능한지 선언



**@interface**

- 어노테이션 선언 시에 사용
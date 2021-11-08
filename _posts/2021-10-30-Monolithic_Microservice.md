---
title: "Monolithic vs MSA"
excerpt: ""
categories:
- MSA
- Monolithic
tags:
- MSA
- Monolithic

---

# Monolithic vs MSA

## Monolith Architecture

모든 업무 로직이 하나의 애플리케이션 형태로 패키지 되어 서비스된다.

애플리케이션에서 사용하는 데이터가 한 곳에 모여 참조되어 서비스되는 형태

![Monolithic Architecture](/assets/images/Monolithic Architecture.png)



**단점**

일부 기능만 수정해도 전체 애플리케이션을 빌드하고 배포해야 함.



## Microserivce

MicroService란 함께 작동하는 작은 규모의 서비스



### Microservice 의 특징

1. Challenges
   - 기존의 개발 방식이나 패러다임을 상당수 변경
2. Small Well Chosen Deployable Units
   - 독립적으로 배포 가능한 작은 서비스로 구성
3. Bounded Context
   - 도메인 지식에 기반한 서비스 경계를 구분
4. RESTful
   - 각각의 서비스들은 REST API 로 통신
5. Configuration Management
   - 환경설정에 대한 내용은 외부의 시스템으로 관리
6. Cloud Enabled
   - Cloud Native 환경을 최대한 활용하여 서비스를 제공
7. Dynamic Scale Up And Scale Down
   - 서비스를 제공하는 인스턴스는 부하분산 처리를 동적으로 처리가 가능해야함
8. CI/CD
9. Visibility
   - 시각화할 수 있는 관리도구를 가지고 있어야함



### MicroService Architecture를 도입하기 전에 고려해야할 사항

1. Multiple Rates of Change

   - 어느 정도의 공수를 들여서 변경할 수 있는가

2. Independent Life Cycles

   - 각각의 어플리케이션이 독립적으로 운영될 수 있는가
   - 도메인 지식을 기반으로 서비스의 경계가 잘 만들어져 있는가

3. Independent Scalability

   - 서비스 유지보수 및 확장성이 보장되는가

4. Isolated Failure

   - 발생하는 오류사항들이 독립적인가

5. Simplify Interactions with External Dependencies

   - 외부 종속성과의 상호작용을 단순화할 수 있는가
   - 서비스간의 종속성을 최소화하고 응집도를 최대화할 수 있는가

6. Polyglot Technology

   - Polyglot 기술을 지원하는가

     

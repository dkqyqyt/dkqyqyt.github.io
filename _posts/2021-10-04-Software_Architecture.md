---
title: "Microservice의 소개"
excerpt: ""
categories:
- MSA
tags:
- MSA
- Software Architecture
---

# Microservice의 소개

## Microservice 란

 ![소프트웨어 아키텍쳐](/assets/images/Software Architecture.png)

Anti-Fragile 문화로 인해 DevOps IT 문화가 생겨났다.



### Antifragile의 특징

- Auto scaling (**자동 확장성**)

  ![Auto scaling](/assets/images/Auto scaling.png)

  여러 개의 인스턴스를 Auto Scaling Group 으로 묶어서 사용

  ex ) 온라인 쇼핑몰 - 5월, 12월과 같은 성수기에는 서버의 갯수를 늘리고 평소에는 서버를 Minimum size로 유지

  수동으로 처리하는 것이 아닌 CPU 또는 메모리, 네트워크, DB 사용량을 통해 자동으로 처리하는 개념.

- Microservices

  ![netflix microservice 구성도](/assets/images/netflix microservice 구성도.png)

  파란색 - 서비스 간의 연동, 통신

  초록색 - netflix를 구성하고 있는 각각의 microservice

- Chaos engineering

  ![Chaos engineering](/assets/images/Chaos engineering.png)

  시스템이  예측하지 못한 상황이라도 견딜 수 있도록 실행하는 방법 또는 규칙

  예견하지 못한 상황에서도 시스템이 안정적으로 유지될 수 있도록 설계해야한다는 의미

- Continuous deployments

  ![Continuous deployments](/assets/images/Continuous deployments.png)

  ex ) CI, CD와 같은 배포 파이프라인


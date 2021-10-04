---
title: "Cloud Native Architecture"
excerpt: ""
categories:
- MSA
tags:
- MSA
- Cloud Native Architecture
---

## Cloud Native Architecture

### 확장 가능한 아키텍처

- 시스템의 수평적 확장에 유연 (scale up - 서버 성능 추가, scale out - 서버 인스턴스 추가)
- 확장된 서버로 시스템의 부하 분산, 가용성 보장
- 시스템 또는 ,서비스 애플리케이션 단위의 패키지 (컨테이너 기반 패키지)
- 모니터링



### 탄력적 아키텍처

- 서비스 생성 - 통합 - 배포, 비즈니스 환경 변화에 대응 시간 단축
- 분할된 서비스 구조
- 무상태 통신 프로토콜
- 서비스의 추가와 삭제 자동으로 감지
- 변경된 서비스 요청에 따라 사용자 요청 처리 (동적 처리)



### 장애 격리 (Fault isolation)

- 특정 서비스에 오류가 발생해도 다른 서비스에 영향을 주지 않음



## Cloud Native Application

![Cloud Native Application](/assets/images/Cloud Native Application.png)



### CI / CD

지속적인 통합 (CI - Continuous Integration)

- 통합 서버, 소스관리 (SCM), 빌드 도구, 테스트 도구
- ex ) Jenkins, Team CI, Travis CI
- 소스를 커밋함과 동시에 빌드, 테스트 실행해서 문제를 바로 확인 가능

지속적 배포

- Continuous Delivery
  - 실행환경으로 소스를 수동으로 반영해야 하는 경우
- Continuous Deployment
  - 실행환경으로 자동으로 소스가 반영되는 경우
- Pipe line

배포 설계 시 고려해야 할 부분

1. 시스템의 정상적인 운영
2. 시스템 다운타임의 최소화

이를 위해서 카나리 배포와 블루그린 배포 방식을 사용

**카나리 배포**

![카나리 배포](/assets/images/카나리 배포.png)

**블루 그린 배포**

![블루 그린 배포](/assets/images/블루 그린 배포.png)

트래픽을 점진적으로 이동



### DevOps

![DevOps](/assets/images/DevOps.png)

![DevOps Pipeline](/assets/images/DevOps Pipeline.png)



### Container 가상화

Cloud Native Application의 핵심

기존의 하드웨어 가상화, 서버 가상화에 비해 적은 리소스를 사용하여 가상화 서비스를 구축 가능

![Container 가상화](/assets/images/Container 가상화.png)


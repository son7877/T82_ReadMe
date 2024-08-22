# T82 Tickets

## 프로젝트 목표

## 진행 기간

2024-07-02 ~ 2024-08- 23

**결제 Service**  https://github.com/T82-encore/T82-payment.git

**쿠폰 Service** https://github.com/T82-encore/T82-Coupon.git

**좌석 Service** https://github.com/T82-encore/T82-Seat.git

**Push 알람 Service**  https://github.com/T82-encore/T82-Push.git

**회원 Service**  https://github.com/T82-encore/T82-User.git

**공연 Service** https://github.com/T82-encore/T82-Event.git

**댓글 Service** https://github.com/T82-encore/T82-Review.git

**티켓 Service**  https://github.com/T82-encore/T82-Ticket.git

**공통 예외 Service** https://github.com/T82-encore/T82-Common-Exception.git

**IOS Service** https://github.com/T82-encore/IOS_T82.git

## 기획 의도

이번 프로젝트의 주요 목표는 콘서트, 연극, 기타 문화 이벤트의 티켓 구매를 ‘조금 더 사용자 친화적이게 공연 예술을 지원하는 것이 어떨까?’ 라는 관점에서 출발 했습니다. **T82**는 많은 고객에게 다양한 문화 생활에 쉽게 접근할 수 있도록 하여 접근성을 높이며, 각 공연의 커뮤니티 참여를 촉진해 많은 사람들에게 문화 생활을 장려하기 위해 기획 되었습니다.

## 협업 관리

저희는 이번 협업 관리를 깃허브의 Project로 진행 하게 되었습니다.
![image (7)](https://github.com/user-attachments/assets/cf3ee942-df71-4a50-a7cc-8782646b34b2)

![image (8)](https://github.com/user-attachments/assets/bce5eeef-eaba-4443-ad05-1c3ae129569e)

![화면 캡처 2024-08-20 125224](https://github.com/user-attachments/assets/8303cff1-8123-482f-abae-d55c89064d1c)

**BackLog : 매 주 마다 개발 해야 할 기능의 목록들의 집합**

**Todo :  그 날 마다 해야 할 기능들의 집합**

**In Progress : 현재 (개발)진행중인 기능들의 집합**

**CodeReview : 개발이 완료되어 merge 되기를 기다리는 기능들의 집합**

**Done : CodeReview를 끝내고 merge 가 된 기능들의 집합**

**Cancled :  BackLog에는 있었지만 진행 도중 취소된 기능들의 집합**

 ****

## 디자인
![image (9)](https://github.com/user-attachments/assets/a09c8cbe-e8c6-47a8-a21d-1d65b0ea6fc4)


## ERD(1차 ~ 최종까지 변경사항)

[https://eastern-orchid-c48.notion.site/T82-Making-4f2615061845453fa3d7ca755da312b7?pvs=4](https://www.notion.so/4f2615061845453fa3d7ca755da312b7?pvs=21)


![image (10)](https://github.com/user-attachments/assets/1e76347a-05a1-45be-98e6-95925d6ab3f6)


이번 프로젝트는 MSA를 도입하게 되었는데 도입하게 된 이유는 아래와 같습니다.

### 도입 이유

### 1. 장애격리

티켓팅 플랫폼의 높은 트래픽에 대한 예상으로 개별 서비스로부터 장애가 옮겨가는 것을 막기 위해 결제 서비스에 문제가 생기더라도 이벤트 조회 등 다른 서비스들은 정상적으로 동작하는 것에 목적을 두어 서비스의 가용성을 높이기 위해 적용 했습니다

### 2. 확장성

MSA의 특징인 각 서비스가 독립적으로 배포되는 것을 이용하기 위해 티켓팅이라는 도메인의 특징인 인기 있는 티켓에 대한 티켓팅이 시작 될 때 이벤트에 관한 서비스만을 확장하여 자원 관리 부분에서 장점이 있을 것으로 생각되어 적용했습니다.

### 3. 트래픽 관리

티켓팅 도메인에서 이벤트 예약이 시작할 때 급증하는 트래픽에 관해서 MSA의 트래픽 분산을 통한 시스템 성능을 유지하는 것을 기대하여 적용하게 되었습니다.

## UserFlow
![t82 UserFlow_v3](https://github.com/user-attachments/assets/c4c37954-4132-451c-a501-2692d60740e8)

## System Architecture
**1차 System Architecture**
![T82 drawio (1)](https://github.com/user-attachments/assets/597ad735-acb7-4eb5-b9f8-45e743040608)


**최종 System Architecture**
![t82아키텍쳐-페이지-2 (5)](https://github.com/user-attachments/assets/0077f317-aa4c-4f7d-b972-1c60604ceb21)

## 사용 기술

1. 프로그래밍 언어 및 프레임워크
![Spring Boot 3](https://img.shields.io/badge/Spring%20Boot-3.0-6DB33F?logo=springboot&logoColor=white)
![Java 17](https://img.shields.io/badge/Java-17-007396?logo=java&logoColor=white)
![Swift 5.1](https://img.shields.io/badge/Swift-5.1-FA7343?logo=swift&logoColor=white)
![SwiftUI](https://img.shields.io/badge/SwiftUI-007AFF?logo=swift&logoColor=white)
[![Spring Security](https://img.shields.io/badge/Spring%20Security-6DB33F?logo=springsecurity&logoColor=white)](https://spring.io/projects/spring-security)
[![Spring Data JPA](https://img.shields.io/badge/Spring%20Data%20JPA-6DB33F?logo=spring&logoColor=white)](https://spring.io/projects/spring-data-jpa)

3. 데이터 베이스
![MySQL](https://img.shields.io/badge/MySQL-4479A1?logo=mysql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?logo=redis&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?logo=firebase&logoColor=white)
[![Mongo DB](https://img.shields.io/badge/Mongo%20DB-47A248?logo=mongodb&logoColor=white)](https://www.mongodb.com/)

5. 클라우드
![Google Cloud Platform](https://img.shields.io/badge/Google%20Cloud-4285F4?logo=googlecloud&logoColor=white)
![AWS Lambda](https://img.shields.io/badge/AWS%20Lambda-FF9900?logo=awslambda&logoColor=white)
![AWS S3](https://img.shields.io/badge/AWS%20S3-569A31?logo=amazons3&logoColor=white)
![AWS EKS](https://img.shields.io/badge/AWS%20EKS-FF9900?logo=amazoneks&logoColor=white)
![AWS API Gateway](https://img.shields.io/badge/AWS%20API%20Gateway-FF4F8B?logo=amazonapigateway&logoColor=white)
[![Nginx](https://img.shields.io/badge/nginx-009639?logo=nginx&logoColor=white)](https://www.nginx.com/)

6. 컨테이너 및 오케스트레이션
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?logo=kubernetes&logoColor=white)
[![Helm](https://img.shields.io/badge/Helm-0F1689?logo=Helm&logoColor=white)](https://helm.sh/)


8. CI/CD
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?logo=jenkins&logoColor=white)
![Xcode Cloud](https://img.shields.io/badge/Xcode%20Cloud-147EFB?logo=xcode&logoColor=white)
![TestFlight](https://img.shields.io/badge/TestFlight-0000FF?logo=testflight&logoColor=white)


9. 메세지 브로커
![Apache Kafka](https://img.shields.io/badge/Apache%20Kafka-231F20?logo=apachekafka&logoColor=white)


10. 부하 테스트 도구
![JMeter](https://img.shields.io/badge/JMeter-D22128?logo=apachejmeter&logoColor=white)

11. 라이브러리
![Feign](https://img.shields.io/badge/Feign-007396?logo=feign&logoColor=white)
![gRPC](https://img.shields.io/badge/gRPC-4285F4?logo=grpc&logoColor=white)
![JitPack](https://img.shields.io/badge/JitPack-4C4C4C?logo=jitpack&logoColor=white)
![Alamofire](https://img.shields.io/badge/Alamofire-FF5722?logo=alamofire&logoColor=white)
![PopupView](https://img.shields.io/badge/PopupView-FF4500?logo=swift&logoColor=white)
![CoreMotion](https://img.shields.io/badge/CoreMotion-007AFF?logo=apple&logoColor=white)
[![Kakao Oauth](https://img.shields.io/badge/Kakao%20Oauth-FFCD00?logo=kakaotalk&logoColor=white)](https://developers.kakao.com/)
[![Google Oauth](https://img.shields.io/badge/Google%20Oauth-4285F4?logo=google&logoColor=white)](https://developers.google.com/identity/protocols/oauth2)

## PPT




## 시연 영상




## 느낀 점 및 트러블 슈팅


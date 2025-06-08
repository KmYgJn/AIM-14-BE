# PITCHING Backend

> 학생들의 협업을 위한 디스코드형 플랫폼 with AI 발표 피드백 기능

## 프로젝트 개요

**개발 기간**: 2024.09.26 ~ 2024.12.25  

## 기술 스택

- **Spring Boot 3.x + Spring WebFlux**
- **Spring Security + JWT**
- **MySQL,AWS DynamoDB, AWS S3**
- **RabbitMQ, WebSocket, Redis**
- **OAuth2** (Naver, Kakao, Google)

## 주요 기능

### 1. 인증 시스템
- JWT (Access + Refresh Token) 기반 무상태 인증
- OAuth2 간편 로그인 (Naver, Kakao, Google)

### 2. 실시간 채팅
- WebSocket 기반 실시간 통신
- RabbitMQ 메시지 큐잉
- DynamoDB 채팅 이력 저장

### 3. AI 발표 피드백
- 음성/영상 데이터 분석
- 실시간 피드백 제공

## 기술적 특징

### Spring WebFlux 선택 이유
- 채팅 시스템에서 대량 동시 연결 처리를 위한 비동기 처리 최적화

### 데이터베이스 전략
- **MySQL**: 사용자 정보, 채팅방 메타데이터
- **DynamoDB**: 채팅 메시지 (높은 처리량, 낮은 지연시간)

### Race Condition 해결
채팅방 인원 제한 시 동시성 문제를 Redis 분산 락으로 해결
- [해결 과정 문서](https://www.notion.so/Race-condition-e3d26441fda04d658b10b747c93bb8f3)

### 테스트
- Jacoco 테스트 커버리지 측정
- [테스트 커버리지 분석](https://www.notion.so/Test-Coverage-136e732830cb80f29762c88b91129ad1)

## 관련 링크
- [프로젝트 문서화](https://www.notion.so/PITCHING-1fee732830cb8082b66df4fc7dbef220)
- [ERD 설계](https://www.notion.so/ERD-976c7dc680224bcb80eb1e6cf44011f0)
- [시스템 아키텍처](https://www.notion.so/10de732830cb80f0a454e3fef277871c)
- [Figma를 통한 UI/UX Design](https://storm-geography-e77.notion.site/Figma-2d37535122944b5cbf7040b58ee7dc83?source=copy_link)

## 홈 화면 (로그인 창)
<img width="1401" alt="Screenshot 2025-06-08 at 8 41 03 PM" src="https://github.com/user-attachments/assets/3b6dd32f-ebe1-4dfe-972f-b082223725c1" />

## 로그인 후 채팅 화면
<img width="1406" alt="Screenshot 2025-06-08 at 8 41 53 PM" src="https://github.com/user-attachments/assets/087f1932-3d53-460a-a327-d14aa11fdbef" />

## 회원 정보 수정 화면
<img width="1408" alt="Screenshot 2025-06-08 at 8 42 21 PM" src="https://github.com/user-attachments/assets/5e4d819f-cd1b-43b8-a548-428174b0b53d" />





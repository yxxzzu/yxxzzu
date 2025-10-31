# ☘ Root - IoT 스마트팜 관리 시스템

> 식물 재배를 위한 스마트팜 관리서비스 시스템 웹 & App 개발 < 업체를 위한 배포용>

IoT 기기를 이용한 스마트팜 모니터링 및 원격제어 시스템으로, 라즈베리파이 기반의 센서 데이터 수집과 자동 제어 기능을 제공합니다.

<br>

## 📋 목차
- [프로젝트 소개](#-프로젝트-소개)
- [주요 기능](#-주요-기능)
- [기술 스택](#-기술-스택)
- [시스템 아키텍처](#-시스템-아키텍처)
- [상세 기능](#-상세-기능)
  - [라즈베리파이 IoT 시스템](#-라즈베리파이-iot-시스템)
  - [웹 관리 시스템](#-웹-관리-시스템)
  - [모바일 앱 원격제어](#-모바일-앱-원격제어)
  - [서비스 신청 시스템](#-서비스-신청-시스템)
  - [일정 관리 캘린더](#-일정-관리-캘린더)
  - [공지사항 관리](#-공지사항-관리)
  - [실시간 문의 시스템](#-실시간-문의-시스템)
- [API 명세](#-api-명세)
- [데이터베이스 구조](#-데이터베이스-구조)
- [실행 방법](#-실행-방법)
<br>

## 🎯 프로젝트 소개

### 개발 기간
**2024.09 ~ 2024.11 (약 2개월)**

![로그인](https://github.com/user-attachments/assets/79f5cdb0-a88d-4ab3-941f-272d377bf61d)
![마이페이지](https://github.com/user-attachments/assets/d838500e-1d84-449c-89ab-38ffb0fc2f8e)

### 개발 목적
농장주가 시간과 장소의 제약 없이 농장 환경을 모니터링하고 원격으로 제어할 수 있는 스마트팜 시스템 구현

<br>

## ✨ 주요 기능
<br>

![일정 캘린더](https://github.com/user-attachments/assets/1d7d4a43-c807-4128-8850-07a4db0a80c8)

### 📅 일정 관리 캘린더
- **개인 일정 등록**: 농장 작업 일정 캘린더에 추가
- **일정 조회**: 월간/주간 단위로 일정 확인
- **일정 관리**: 등록된 일정 수정 및 삭제 가능
- **날짜별 필터링**: 특정 날짜의 작업 내역 조회
<br>

![서비스 신청](https://github.com/user-attachments/assets/b972d2cf-027d-4292-b755-cdf8ff487119)

### 📝 서비스 신청 관리
- **신청서 작성**: 개인/법인 구분하여 서비스 신청 가능
- **신청 현황 확인**: 신청 날짜, 승인 여부 실시간 조회
- **관리자 승인 시스템**: 관리자의 신청 승인/거부 처리

<br>

![공지사항](https://github.com/user-attachments/assets/71f98e9a-f8ae-47b6-b661-c8c0621a5075)

### 📢 공지사항
- **관리자 공지 작성**: 이미지 첨부 가능한 공지사항 게시
- **공지사항 조회**: 전체 회원 대상 중요 공지 확인
- **첨부 파일 지원**: 사진, 문서 등 파일 첨부 기능

![실시간 통신](https://github.com/user-attachments/assets/d1e19ad5-15a8-45d4-a7da-3312cab60812)

### 💬 실시간 문의 시스템
- **실시간 문의 등록**: 사용자의 문의사항 즉시 등록 (WebSocket)
- **실시간 알림**: 문의 등록 시 관리자에게 즉시 알림
- **실시간 답변**: 관리자 답변 시 사용자에게 즉시 알림
- **문의 이력 관리**: 과거 문의 내역 조회 가능

### ⚙ 자동 환경 제어
- **온습도 기반 자동 환경 조절**: 설정값 초과 시 쿨링팬 자동 작동
- **토양 수분 관리**: 수분 부족 시 워터펌프 자동 작동
- **조도 관리**: 조도 부족 시 LED 자동 점등
- **보안 시스템**: 적외선 센서로 움직임 감지 시 부저 알림

### 📱 원격 모니터링 & 제어
- **실시간 센서 데이터 모니터링**: 온도, 습도, 토양수분, 조도 데이터 실시간 확인
- **원격 기준값 설정**: 웹/앱에서 자동 제어 기준값 설정 가능
- **수동/자동 모드 전환**: 자동 제어 ON/OFF 및 수동 제어 지원
- **Push 알림**: 이상 상황 발생 시 앱으로 즉시 알림

### 💬 AI 식물 인식 챗봇
- **PlantNet API 연동**: 식물 사진 업로드 시 자동 인식
- **식물 정보 제공**: 학명, 일반명, 과 정보 제공
- **대화형 인터페이스**: 챗봇 방식으로 편리한 사용자 경험 제공

### 👥 관리자 기능
- **회원 관리**: 회원 목록 조회, 검색, 일괄/선택 삭제
- **서비스 신청 관리**: 신청 목록 조회, 검색, 승인 처리
- **대시보드**: 실시간 센서 데이터 및 7일 기준 통계 시각화

<br>

## 🛠 기술 스택

### 🖥️ Backend
![Java](https://img.shields.io/badge/Java_17-007396?style=for-the-badge&logo=java&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot_3.4-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![MyBatis](https://img.shields.io/badge/MyBatis-000000?style=for-the-badge&logo=mybatis&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![WebSocket](https://img.shields.io/badge/WebSocket-010101?style=for-the-badge&logo=socketdotio&logoColor=white)

### 🎨 Frontend - Web
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Axios](https://img.shields.io/badge/Axios-5A29E4?style=for-the-badge&logo=axios&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

### 📱 Frontend - Mobile
![React Native](https://img.shields.io/badge/React_Native-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Expo](https://img.shields.io/badge/Expo-000020?style=for-the-badge&logo=expo&logoColor=white)

### 🔌 IoT
![Raspberry Pi](https://img.shields.io/badge/Raspberry_Pi-A22846?style=for-the-badge&logo=raspberry-pi&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

### 🌐 External API
![PlantNet](https://img.shields.io/badge/PlantNet_API-4CAF50?style=for-the-badge&logo=leaflet&logoColor=white)

---

## 🏗️ 시스템 아키텍처

### 전체 구조
```
[Raspberry Pi]  ←→  [Spring Boot Backend]  ←→  [Web Admin / Mobile App]
   (Python)          WebSocket + REST API         (React / React Native)
      ↓                      ↓                              ↓
  센서/제어기            MariaDB/Redis              PlantNet API
```

### 데이터 흐름

**1. 센서 → 백엔드 → DB**
- Raspberry Pi에서 센서 데이터 수집 (1~2초 간격으로 체크/60분 간격으로 DB 저장)
- WebSocket으로 Spring Boot에 전송
- MariaDB GROWING 테이블에 저장

**2. 웹/앱 → 백엔드 → 라즈베리파이**
- 사용자가 웹/앱에서 제어 명령 전송
- REST API로 백엔드 전달
- WebSocket으로 Raspberry Pi에 명령 전송

**3. 알림 전송**
- 센서 값이 임계값 초과
- 자동 제어 시스템 작동
- FCM을 통해 앱에 푸시 알림 전송

---

## 🔌 라즈베리파이 IoT 시스템

### 📡 센서 구성

| 센서 | 측정 항목 | GPIO 핀 | 임계값(설정) |
|------|----------|---------|--------|
| DHT22 | 온도/습도 | GPIO 4 | 28°C / 70% |
| 토양수분센서 | 토양 수분도 | GPIO 17 | 30% |
| 조도센서 | 조도 (Lux) | GPIO 27 | 300 Lux |
| PIR 모션센서 | 움직임 감지 | GPIO 22 | - |

### ⚙️ 자동 제어 로직

#### 온도 제어
```
조건: 온도 ≥ 28°C (사용자 설정값)
동작: 팬 모터 작동
알림: 앱 푸시 알림 전송 (알림 표시방식 설정 가능)
```

#### 토양 수분 제어
```
조건: 토양 수분 ≤ 30% (사용자 설정값)
동작: 워터펌프 5초 작동
알림: 앱 푸시 알림 전송 (알림 표시방식 설정 가능)
```

#### 조도 제어
```
조건: 조도 ≤ 300 Lux (사용자 설정값)
동작: LED 점등
알림: 앱 푸시 알림 전송 (알림 표시방식 설정 가능)
```

#### 모션 감지
```
조건: 적외선 센서 감지
동작: 부저 알림음 0.5초 작동
알림: 앱 즉시 알림 전송
```

### 🔌 WebSocket 통신

#### Python → Spring Boot 데이터 전송

**센서 데이터 JSON 형식**
```json
{
  "temperature": 26.5,
  "humidity": 65.2,
  "soilHumidity": 45.0,
  "illumination": 450
}
```

**전송 주기**: 1분마다  
**저장 위치**: MariaDB GROWING 테이블

---

## 💻 웹 관리 시스템

### 👥 회원 관리

#### 기능
- **목록 조회**: 전체 회원 목록 확인 (USER/ADMIN 구분)
- **검색**: 회원명으로 부분 일치 검색
- **서비스 이용 상태**: LEFT JOIN으로 서비스 신청 여부 표시
- **일괄/선택 삭제**: 체크박스로 선택 후 삭제

#### API 엔드포인트
```
GET    /users/userList              # 회원 목록 조회
GET    /users/userList/{userName}   # 회원명 검색
DELETE /users/delete/{userId}       # 회원 삭제
GET    /users/weekly                # 최근 7일 신규 가입자 수
```

#### 주요 특징
- 전체 선택 시 개별 체크박스 자동 선택
- 일부 해제 시 전체 선택 체크박스 자동 해제
- 서비스 이용 여부 "이용 중" / "-" 표시

---

### 📋 서비스 신청 관리

#### 기능
- **신청 목록 조회**: 전체 서비스 신청 현황 확인
- **검색**: 신청자명으로 검색
- **승인 처리**: 승인 버튼 클릭 시 승인일 자동 기록
- **버튼 비활성화**: 승인 완료된 항목은 버튼 비활성화

#### API 엔드포인트
```
GET /applications/list                  # 신청 목록 조회
GET /applications/appList/{userName}    # 신청자명 검색
PUT /applications/approve/{applNum}     # 승인 처리
```

#### 주요 특징
- 승인 시 `APPR_DATE = NOW()` 자동 입력
- 승인 후 목록 자동 새로고침
- "대기 중" / "승인 완료" 시각적 구분

---

### 💬 AI 식물 인식 챗봇

#### 기능
- **세션 관리**: UUID 기반 사용자별 채팅방 생성
- **이미지 인식**: PlantNet API로 식물 사진 분석
- **결과 표시**: 학명, 일반명, 과(科), 신뢰도(%) 제공
- **텍스트 대화**: 간단한 키워드 기반 응답

#### API 엔드포인트
```
POST /api/chat/session                      # 세션 생성
POST /api/chat/session/{sessionId}/image    # 이미지 업로드 (식물 인식)
POST /api/chat/session/{sessionId}/message  # 텍스트 메시지
GET  /api/chat/session/{sessionId}/messages # 대화 이력 조회
```

#### 주요 특징
- **API 키 보안**: 백엔드에서 환경변수로 관리
- **파일 검증**: 이미지 타입 체크, 5MB 크기 제한
- **CORS 설정**: `@CrossOrigin`으로 프론트-백 통신 허용
- **HTML 스타일링**: 신뢰도 배지, 색상 구분

---

## 📱 모바일 앱 원격제어

https://github.com/user-attachments/assets/48ddccbe-41db-4a5e-951a-0db03002b8c4

### 환경 원격제어

#### 기능
- **실시간 조회**: 현재 센서 데이터 1분마다 자동 갱신
- **기준값 설정**: 온도, 습도, 토양수분, 조도 임계값 설정
- **자동/수동 전환**: 자동 제어 ON/OFF 스위치
- **웹-앱 동기화**: 웹에서 설정한 기준값과 동기화

#### 화면 구성
- **센서 현황**: 온도, 습도, 토양수분, 조도 실시간 표시
- **제어 모드**: 자동/수동 토글 스위치
- **기준값 입력**: 각 센서별 임계값 입력 필드
- **저장 버튼**: 기준값 서버 저장

---

### 🔔 푸시 알림

#### 알림 종류
| 상황 | 알림 메시지 |
|------|------------|
| 온도 초과 | ⚠️ 온도 이상 감지 - 현재 30.5°C (기준 28°C) |
| 토양 건조 | 💧 토양 수분 부족 - 현재 25% (기준 30%) |
| 조도 부족 | 💡 조도 부족 - LED 자동 점등 |
| 모션 감지 | 🚨 움직임 감지 - 부저 작동 |

---

## 📝 서비스 신청 시스템

### 기능
- **신청서 작성**: 개인/법인 선택, 농장명, 연락처, 주소 입력
- **신청 유형**: PERSONAL(개인) / CORPORATE(법인) 구분
- **신청 현황**: 신청일, 승인일, 승인 상태 확인
- **관리자 승인**: 관리자 페이지에서 승인 처리

### API 엔드포인트
```
POST /applications/register           # 서비스 신청
GET  /applications/myList/{userId}    # 내 신청 내역 조회
GET  /applications/list               # 전체 신청 목록 (관리자)
PUT  /applications/approve/{applNum}  # 승인 처리 (관리자)
```

---

## 📅 일정 관리 캘린더

### 기능
- **일정 등록**: 제목, 내용, 시작일, 종료일 설정
- **캘린더 뷰**: 월간 캘린더로 일정 시각화
- **일정 조회**: 특정 날짜 클릭 시 해당 날짜 일정 표시
- **일정 수정/삭제**: 등록된 일정 관리

### API 엔드포인트
```
POST   /schedules/register         # 일정 등록
GET    /schedules/list/{userId}    # 내 일정 목록 조회
GET    /schedules/{scheduleId}     # 일정 상세 조회
PUT    /schedules/update           # 일정 수정
DELETE /schedules/delete/{scheduleId}  # 일정 삭제
```

### 주요 특징
- 월별 일정 필터링
- 날짜별 일정 개수 표시
- 작업 일정 관리 최적화

---

## 📢 공지사항 관리

### 기능
- **공지 작성**: 제목, 내용, 이미지 첨부 (관리자)
- **공지 조회**: 전체 회원 대상 공지사항 목록
- **이미지 업로드**: 다중 이미지 첨부 지원
- **공지 검색**: 제목/내용 기반 검색

### API 엔드포인트
```
POST   /notices/register           # 공지 등록 (관리자)
GET    /notices/list               # 공지 목록 조회
GET    /notices/{noticeId}         # 공지 상세 조회
PUT    /notices/update             # 공지 수정 (관리자)
DELETE /notices/delete/{noticeId}  # 공지 삭제 (관리자)
```

### 주요 특징
- 파일 업로드: `MultipartFile` 처리
- 이미지 저장 경로: `/upload/notice/`
- 페이지네이션 지원

---

## 💬 실시간 문의 시스템

### 기능
- **문의 등록**: 제목, 내용 입력 후 실시간 전송
- **실시간 알림**: WebSocket으로 관리자에게 즉시 알림
- **실시간 답변**: 관리자 답변 시 사용자에게 즉시 알림
- **문의 이력**: 과거 문의/답변 내역 조회

### API 엔드포인트
```
POST /questions/register          # 문의 등록
GET  /questions/list              # 문의 목록 조회 (관리자)
GET  /questions/myList/{userId}   # 내 문의 내역 조회
POST /answers/register            # 답변 등록 (관리자)
```

### WebSocket 통신
```javascript
// 문의 등록 시 알림
stompClient.send("/app/question/notify", {}, JSON.stringify({
  questionId: questionId,
  userId: userId,
  message: "새로운 문의가 등록되었습니다."
}));

// 답변 등록 시 알림
stompClient.send("/app/answer/notify", {}, JSON.stringify({
  questionId: questionId,
  message: "답변이 등록되었습니다."
}));
```

### 주요 특징
- **WebSocket 기반** 실시간 양방향 통신
- 문의 등록 시 → 관리자 알림
- 답변 등록 시 → 사용자 알림
- 읽음/미읽음 상태 표시

---

## 📡 API 명세

### 센서 데이터

| Method | Endpoint | 설명 |
|--------|----------|------|
| GET | `/growings` | 전체 센서 데이터 조회 |
| GET | `/growings/weekly` | 최근 7일 데이터 조회 |
| GET | `/growings/rev` | 역순 정렬 데이터 조회 |

### 회원 관리

| Method | Endpoint | 설명 |
|--------|----------|------|
| GET | `/users/userList` | 회원 목록 조회 |
| GET | `/users/userList/{userName}` | 회원명 검색 |
| DELETE | `/users/delete/{userId}` | 회원 삭제 |

### 서비스 신청

| Method | Endpoint | 설명 |
|--------|----------|------|
| POST | `/applications/register` | 서비스 신청 |
| GET | `/applications/list` | 신청 목록 조회 |
| PUT | `/applications/approve/{applNum}` | 승인 처리 |
| GET | `/applications/appList/{userName}` | 신청자명 검색 |

### 일정 관리

| Method | Endpoint | 설명 |
|--------|----------|------|
| POST | `/schedules/register` | 일정 등록 |
| GET | `/schedules/list/{userId}` | 내 일정 목록 조회 |
| GET | `/schedules/{scheduleId}` | 일정 상세 조회 |
| PUT | `/schedules/update` | 일정 수정 |
| DELETE | `/schedules/delete/{scheduleId}` | 일정 삭제 |

### 공지사항

| Method | Endpoint | 설명 |
|--------|----------|------|
| POST | `/notices/register` | 공지 등록 (관리자) |
| GET | `/notices/list` | 공지 목록 조회 |
| GET | `/notices/{noticeId}` | 공지 상세 조회 |
| PUT | `/notices/update` | 공지 수정 (관리자) |
| DELETE | `/notices/delete/{noticeId}` | 공지 삭제 (관리자) |

### 문의 시스템

| Method | Endpoint | 설명 |
|--------|----------|------|
| POST | `/questions/register` | 문의 등록 |
| GET | `/questions/list` | 문의 목록 조회 (관리자) |
| GET | `/questions/myList/{userId}` | 내 문의 내역 조회 |
| POST | `/answers/register` | 답변 등록 (관리자) |

### AI 챗봇

| Method | Endpoint | 설명 |
|--------|----------|------|
| POST | `/api/chat/session` | 세션 생성 |
| POST | `/api/chat/session/{sessionId}/image` | 식물 인식 |
| POST | `/api/chat/session/{sessionId}/message` | 텍스트 메시지 |

### 모션 감지

| Method | Endpoint | 설명 |
|--------|----------|------|
| GET | `/motions` | 감지 로그 조회 |
| GET | `/motions/stats` | 감지 통계 조회 |
| GET | `/motions/today` | 오늘 감지 횟수 |

---

## 🗄️ 데이터베이스 구조

### 주요 테이블

#### USERS (회원)
- `USER_ID` (PK): 사용자 ID
- `USER_PW`: 암호화된 비밀번호 (BCrypt)
- `USER_NAME`: 이름
- `USER_EMAIL`: 이메일
- `USER_ROLE`: 권한 (USER/ADMIN)
- `CREATE_DATE`: 가입일

#### APPLICATION (서비스 신청)
- `APPL_NUM` (PK): 신청 번호
- `USER_ID` (FK): 신청자 ID
- `FARM_NAME`: 농장명
- `APPL_ROLE`: 유형 (PERSONAL/CORPORATE)
- `BUSINESS_TEL`: 연락처
- `APPL_ADDR`: 주소
- `REG_DATE`: 신청일
- `APPR_DATE`: 승인일

#### SCHEDULE (일정)
- `SCHEDULE_ID` (PK): 일정 번호
- `USER_ID` (FK): 사용자 ID
- `TITLE`: 일정 제목
- `CONTENT`: 일정 내용
- `START_DATE`: 시작일
- `END_DATE`: 종료일
- `CREATE_DATE`: 등록일

#### NOTICE (공지사항)
- `NOTICE_NUM` (PK): 공지 번호
- `NOTICE_TITLE`: 제목
- `NOTICE_CONTENT`: 내용
- `NOTICE_DATE`: 작성일
- `ATTACHED_FILE`: 첨부파일

#### QUESTION (문의)
- `QUESTION_NUM` (PK): 문의 번호
- `USER_ID` (FK): 작성자 ID
- `QUESTION_TITLE`: 제목
- `QUESTION_CONTENT`: 내용
- `REG_DATE`: 등록일
- `IS_ANSWERED`: 답변 여부

#### ANSWER (답변)
- `ANSWER_NUM` (PK): 답변 번호
- `QUESTION_NUM` (FK): 문의 번호
- `ANSWER_CONTENT`: 답변 내용
- `REG_DATE`: 등록일

#### GROWING (센서 데이터)
- `TEMPER_NUM` (PK): 데이터 번호
- `TEMPER`: 온도 (°C)
- `HUMIDITY`: 습도 (%)
- `SOIL_HUMIDITY`: 토양 수분 (%)
- `ILLUMINATION`: 조도 (Lux)
- `CREATE_DATE`: 측정 시간

#### MOTION_BUZZER (모션 감지)
- `MOTION_NUM` (PK): 감지 번호
- `DETECT_DATE`: 감지 시간

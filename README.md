# 라즈베리 파이 피코 프로젝트

사내/로컬 환경에서 사용하던 프로젝트로, 코드 공개는 제한하고 개요만 정리했습니다.

## ✅ 프로젝트 소개
> **라즈베리 파이 피코**와 **온/습도 센서**를 이용한 사무실 환경 제어 프로젝트

### 프로젝트 목표
- 온/습도 센서를 통해 사무실 내 환경 데이터를 실시간으로 수집하고 모니터링한다.
- 수집된 데이터를 분석하여 효율적으로 사무실 환경을 관리한다.

### 기대 효과
사무실 내 온/습도로 인해 발생할 수 있는 불편함을 줄이고, 자동화된 환경 제어를 통해 최적의 업무 환경을 유지할 수 있도록 한다. 
이를 통해 근무자의 업무 효율성 향상 및 건강 관리를 돕고, 에너지 절감에도 기여할 수 있다.

## ✅ 설계 명세
### 시스템 아키텍처
![](https://velog.velcdn.com/images/yjseo01/post/2e51ff01-446a-4f77-a6a3-5bc3d062a789/image.png)

### 데이터베이스 설계 

#### 1. **Bucket**
![](https://velog.velcdn.com/images/yjseo01/post/11b322b7-e28c-49b9-a087-e91bf99d55fe/image.png)

#### 2. **Measurements**
![](https://velog.velcdn.com/images/yjseo01/post/495b8d5e-1092-42ef-80dd-0a26306dbc32/image.png)


## ✅ 구현
### 개발 환경 및 기술 스택
#### 하드웨어

- 센서
    - 온/습도 센서
- 마이크로컨트롤러
    - 라즈베리 파이 피코 (Raspberry Pi Pico W)

#### 임베디드 소프트웨어

- 프로그래밍 언어
    - C
- SDK 및 툴체인
    - Raspberry Pi Pico SDK: 마이크로컨트롤러 프로그램 개발을 위한 C언어 SDK
    - Visual Studio Code: 코드 작성 및 디버깅.
- 시리얼 통신 프로토콜
    - UART (Universal Asynchronous Receiver-Transmitter)
- 네트워크 프로토콜 라이브러리
    - lwIP: Lightweight IP stack, TCP/IP 기반 네트워크 통신 제공
    - MQTT: lwIP의 mqtt.h
    - HTTP: lwIP의 httpd.h
    - NTP: lwIP의 sntp.h

#### MQTT 브로커 (서버)
- 브로커
    - Mosquitto
- 운영체제
    - Windows

#### 데이터 저장 및 처리
- 데이터베이스
    - influxDB

#### 대시보드
- 프로그래밍 언어
    - C#
- MQTT 클라이언트 라이브러리
    - MQTTNet
- 사용자 인터페이스 (UI)
    - Blazor, Radzen
- 실시간 일림 구현
    - Signal R
- 운영체제
    - Windows

## ✅ 일정
![](https://velog.velcdn.com/images/yjseo01/post/cc3e4ef9-594b-4d8c-ab07-2b3c3b339046/image.png)

## ✅ 실행 화면
### 홈 화면
![](https://velog.velcdn.com/images/yjseo01/post/070db962-86c4-4d77-bb3e-22e1153e0929/image.png)

### 모니터링 화면
![](https://velog.velcdn.com/images/yjseo01/post/791cc4fd-82d9-4437-9671-0aed0456d9a7/image.png)

### 보고서 화면
![](https://velog.velcdn.com/images/yjseo01/post/691e0b64-585a-4c80-896b-14099fd5f086/image.png)

![](https://velog.velcdn.com/images/yjseo01/post/eda4e030-72e7-4369-bd01-f6461a5488a0/image.png)


### 설정 화면
![](https://velog.velcdn.com/images/yjseo01/post/869fdced-f445-4cf7-9526-78d08ae53c1e/image.png)


### 알림
![](https://velog.velcdn.com/images/yjseo01/post/5d3e238d-8e58-4b84-82bf-3f5a0c0cd403/image.png)


## ✅ 레퍼런스
🔗https://github.com/dotnet/MQTTnet

🔗https://github.com/raspberrypi/pico-examples

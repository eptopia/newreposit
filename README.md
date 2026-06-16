# Linux 명령어 탐구 과제

| 명령어 | 기능 |
|---------|---------|
| top | 실행 중인 프로세스와 시스템 자원 사용 현황을 실시간으로 확인 |
| ps | 현재 실행 중인 프로세스 정보 출력 |
| jobs | 현재 쉘의 백그라운드 작업 확인 |
| kill | 실행 중인 프로세스 종료 |

---

## 1. top

| 항목 | 설명 |
|---------|---------|
| 목적 | 시스템 상태와 프로세스 정보를 실시간으로 모니터링 |
| 사용법 | `top` |
| 확인 가능 정보 | PID, CPU 사용량, 메모리 사용량, 실행 시간 등 |
| 특징 | 실시간 갱신 |

### 예시

```bash
top
```
### 실행화면
(bash에서는 실행되지 않아 JSLINUX라는 웹사이트를 이용했습니다.)

<img width="1194" height="1031" alt="스크린샷 2026-06-16 162256" src="https://github.com/user-attachments/assets/e2f1e3f9-f070-46b5-b09c-f18287c990a9" />

---

## 2. ps


| 항목 | 설명 |
|---------|---------|
| 목적 | 프로세스 정보 조회 |
| 사용법 | `ps`, `ps -e`, `ps aux` |
| 확인 가능 정보 | PID, 사용자, CPU 사용량, 프로세스 상태 |
| 특징 | 현재 시점의 프로세스 정보 출력 |

### 예시

```bash
ps 
```
### 실행화면

<img width="1130" height="173" alt="ps png" src="https://github.com/user-attachments/assets/59605289-25fa-42d5-ba2b-249d83b2d13c" />

---

## 3. jobs

| 항목 | 설명 |
|---------|---------|
| 목적 | 백그라운드 작업 확인 |
| 사용법 | `jobs` |
| 확인 가능 정보 | Job ID, 작업 상태 |
| 특징 | 현재 쉘에서 실행 중인 작업만 표시 |

### 예시

```bash
sleep 100 &
jobs
```
### 실행화면

<img width="637" height="103" alt="jobs png" src="https://github.com/user-attachments/assets/3baff641-b9ea-4610-91ce-364de2af82b9" />

---

## 4. kill


| 항목 | 설명 |
|---------|---------|
| 목적 | 프로세스 종료 |
| 사용법 | `kill PID` |
| 주요 옵션 | `-15` 정상 종료, `-9` 강제 종료 |
| 특징 | 특정 프로세스에 시그널 전달 |

### 예시

```bash
kill 581
```
### 실행화면
<img width="632" height="189" alt="kill png" src="https://github.com/user-attachments/assets/244dae04-d1bf-4b2e-bfa3-be47baeb2896" />

---

## 명령어 비교

| 명령어 | 실시간 확인 | 프로세스 조회 | 작업 관리 | 종료 기능 |
|---------|---------|---------|---------|---------|
| top | O | O | X | X |
| ps | X | O | X | X |
| jobs | X | X | O | X |
| kill | X | X | X | O |

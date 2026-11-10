# 팀 규칙

가볍게 지키는 권장 규칙입니다. 강제되는 건 아래 "레포 보호 설정"뿐입니다.

## 레포

| 레포 | 용도 |
| --- | --- |
| [Docs](https://github.com/Course-Registration-System/Docs) | 계획서, 설계 산출물, 보고서 |
| [Backend](https://github.com/Course-Registration-System/Backend) | 서버, DB |
| [Frontend](https://github.com/Course-Registration-System/Frontend) | 웹 화면 |

## 기술 스택

| 구분 | 내용 |
| --- | --- |
| Backend | Java 21, Spring Boot 4.1 (Web MVC, JdbcTemplate, Validation), Gradle. ORM(JPA)·Lombok 은 쓰지 않고 SQL 을 직접 작성 |
| Frontend | React 19, TypeScript, Vite 8 |
| DB | MySQL 8.4 (테스트는 H2 인메모리) |

실행 방법은 각 레포 README에 있습니다. 로컬에서는 백엔드 8080, 프론트 5173 포트를 쓰고, 프론트의 `/api` 요청은 백엔드로 프록시됩니다.

## 레포 보호 설정 (main 브랜치)

| | Docs | Backend / Frontend |
| --- | --- | --- |
| main 직접 푸시 | 허용 | PR로만 병합 |
| PR 승인 | 필요 없음 | 0명 (리뷰 권장) |
| 강제 푸시·브랜치 삭제 | 차단 | 차단 |
| 조직 관리자 우회 | 가능 | 가능 |

병합은 squash 또는 merge commit을 쓰고, 병합된 브랜치는 자동 삭제됩니다.

## 브랜치 이름

`종류/짧은-설명` 형식을 권장합니다.

- `feat/enrollment-api` 기능 추가
- `fix/timetable-overlap` 버그 수정
- `docs/logical-model` 문서
- `chore/setup` 설정·기타

## 커밋 메시지

`종류: 내용` 형식, 한글 OK.

```
feat: 수강신청 API 추가
fix: 시간표 중복 검사 오류 수정
docs: 논리적 데이터 모델 추가
```

## 이슈·PR

- 작업 전 이슈를 만들고 PR 본문에 `#이슈번호`를 적으면 좋습니다.
- 라벨: `BE`, `FE`, `Docs`, `priority:high`
- 오래 걸리는 PR은 Draft로 먼저 올려 공유합니다.

## 금지

- `.env`, 비밀번호, DB 접속 정보 커밋
- main 강제 푸시

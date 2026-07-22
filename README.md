# Claude Todo Web Project

Claude Code와 함께 만든 심플한 할 일 목록(Todo List) 웹 앱입니다.
별도 설치나 서버 없이 `index.html` 파일 하나로 동작하며, 데이터는 Supabase 데이터베이스에 저장됩니다.

## ✨ 주요 기능

- 할 일 추가 / 수정 / 삭제
- 완료 체크 (완료 처리)
- 카테고리별 분류
- 필터 탭으로 보기 전환 (전체 / 진행중 / 완료 등)
- 진행률(progress) 표시
- Supabase 데이터베이스(`todo_tbl` 테이블)에 저장 → 어떤 기기에서 접속해도 동일한 데이터 확인 가능

## 🛠 기술 스택

- HTML / CSS / Vanilla JavaScript (프레임워크 없음)
- 데이터 저장: [Supabase](https://supabase.com) (Postgres 기반), `supabase-js` 클라이언트를 CDN으로 로드
- 접근 제어: Supabase Row Level Security(RLS) 정책 + anon(publishable) key

## 🚀 사용 방법

1. 이 저장소를 clone 하거나 `index.html` 파일을 다운로드합니다.
2. `index.html` 파일을 웹 브라우저로 엽니다.
3. 별도 설치나 빌드 과정 없이 바로 사용할 수 있습니다. (Supabase 프로젝트 URL과 anon key는 이미 코드에 포함되어 있습니다.)

## 📁 구조

```
claude-todo-web-pjt/
└── index.html   # 할 일 목록 앱 (HTML+CSS+JS 단일 파일, Supabase 연동)
```

## 🗄 데이터베이스 스키마 (`todo_tbl`)

| 컬럼 | 타입 | 설명 |
| --- | --- | --- |
| id | bigint (identity) | 기본 키 |
| text | text | 할 일 내용 |
| category | text | 개인 / 공부 / 업무 / 취미 중 하나 |
| completed | boolean | 완료 여부 (기본값 false) |
| created_at | timestamptz | 생성 시각 (기본값 now()) |

---
Claude Code로 제작되었습니다.

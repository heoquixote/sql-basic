# 00. 저장소 사용 방법

이 페이지는 `sql-basic` 저장소를 WikiDocs와 함께 운영할 때 참고하는 기본 가이드입니다.

## 작성 흐름

1. `TOC.md`에서 장과 페이지 순서를 먼저 정의합니다.
2. 실제 본문은 `pages/` 디렉토리에 추가합니다.
3. 이미지는 `assets/`에 저장하고 상대 경로로 연결합니다.
4. 변경사항을 GitHub에 push하면 WikiDocs 반영 흐름과 함께 관리할 수 있습니다.

## 마크다운 작성 팁

- 제목은 `#`으로 시작합니다.
- 목록은 `-` 또는 `*`로 작성합니다.
- 코드는 백틱으로 감싸거나 코드 블록으로 작성합니다.

## 페이지 순서 유지

WikiDocs에서는 페이지 제목과 파일명이 정렬에 영향을 줄 수 있으므로,
가능하면 `01`, `02`, `03`처럼 번호 체계를 일관되게 맞추는 편이 안전합니다.

예를 들어:

- `01-sql-thinking-and-execution-order.md`
- `02-sql-environment-and-practice-data.md`
- `03-basic-query-patterns.md`

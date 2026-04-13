# 목차

* [01. SQL 사고방식과 실행 순서](pages/01-sql-thinking-and-execution-order.md)
  * SQL은 왜 읽는 순서와 실행 순서가 다른가
  * FROM, WHERE, GROUP BY, HAVING, SELECT, ORDER BY
  * 행 단위 사고와 집계 단위 사고
* [02. SQL 실습 환경과 연습 데이터](pages/02-sql-environment-and-practice-data.md)
  * 어떤 DBMS로 연습할 것인가
  * 샘플 스키마 읽는 법
  * 기본 키, 외래 키, 그레인 확인
* [03. 기본 조회와 필터링](pages/03-basic-query-patterns.md)
  * SELECT, DISTINCT, WHERE, ORDER BY, LIMIT
  * NULL과 비교 연산
  * 날짜, 문자열, 숫자 조건 처리
* [04. JOIN과 집합 연산](pages/04-join-and-set-operations.md)
  * INNER / LEFT / RIGHT / FULL JOIN
  * UNION vs UNION ALL
  * 중복 행과 카디널리티 문제
* [05. 집계와 지표 계산](pages/05-aggregation-and-business-metrics.md)
  * COUNT, SUM, AVG, MIN, MAX
  * GROUP BY와 HAVING
  * 비율, 전환율, 분모 정의
* [06. 서브쿼리와 CTE](pages/06-subquery-and-cte.md)
  * 인라인 서브쿼리
  * 상관 서브쿼리
  * WITH 절과 단계별 질의 설계
* [07. 윈도우 함수](pages/07-window-functions.md)
  * ROW_NUMBER, RANK, DENSE_RANK
  * 누적값과 이동 평균
  * LAG / LEAD와 시계열 비교
* [08. 함수와 데이터 정제](pages/08-data-cleaning-and-built-in-functions.md)
  * CASE, COALESCE, NULLIF
  * 문자열 함수와 날짜 함수
  * 정제 로직을 SQL에 둘지 ETL에 둘지
* [09. 스키마 해석과 데이터 모델링](pages/09-schema-modeling-and-granularity.md)
  * 팩트와 차원
  * 정규화와 비정규화
  * 그레인과 조인 안정성
* [10. 성능 최적화와 실행 계획](pages/10-query-performance-and-optimization.md)
  * 인덱스와 스캔
  * 불필요한 DISTINCT와 중복 정렬 줄이기
  * 실행 계획에서 먼저 볼 것
* [11. 실무 분석 SQL 패턴](pages/11-practical-analysis-recipes.md)
  * 코호트와 리텐션
  * 퍼널 분석
  * 재구매와 활성 사용자
* [12. BI / 리포팅 / 데이터 워크플로우에서의 SQL](pages/12-sql-in-bi-and-data-workflows.md)
  * 대시보드용 SQL
  * 데이터 마트 적재용 SQL
  * 지표 정의와 검증용 SQL
